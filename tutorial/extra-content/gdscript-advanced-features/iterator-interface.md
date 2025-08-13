# 迭代器接口

```gdscript
class_name StaticArray

var count: int
var is_empty: bool

var _arr : Array
var _iter_index: int = 0

func set_element(index: int, value: Variant) -> void:   
    assert(_arr != null, "StaticArray is not initialized.")
    assert(index >= 0, "Index must be non-negative.")
    assert(index < _arr.size(), "Index out of bounds: " + str(index))
    assert(typeof(value) == _arr.get_typed_builtin(), "Type mismatch.")
    if value is Object:
        assert(value.get_class() == _arr.get_typed_class_name(), "Type mismatch.")
        assert(value.get_script() == _arr.get_typed_script(), "Type mismatch.")
    _arr[index] = value

func get_element(index: int) -> Variant:
    assert(_arr != null, "StaticArray is not initialized.")
    assert(index >= 0, "Index must be non-negative.")        
    assert(index < _arr.size(), "Index out of bounds: " + str(index))    
    return _arr[index]

func _init(from: Array) -> void:
    _arr = Array(from.duplicate(true), from.get_typed_builtin(), from.get_typed_class_name(), from.get_typed_script())
    _arr.resize(from.size())
    count = from.size()
    is_empty = count == 0

func _notification(what: int) -> void:
    if what == NOTIFICATION_PREDELETE:
        _arr.clear()
        _iter_index = 0        

func _to_string() -> String:
    return "StaticArray(" + str(_arr) + ")"

func _iter_init(iter: Array) -> bool:
    if _arr.is_empty():
        return false
    _iter_index = 0
    iter[0] = _arr[0]       
    return true

func _iter_next(iter: Array) -> bool:
    _iter_index += 1
    if _iter_index >= _arr.size():
        return false
    iter[0] = _arr[_iter_index] 
    return true

func _iter_get(iter: Variant) -> Variant:
    return iter

```

在 GDScript 中，如果你希望让一个自定义对象能被 `for ... in ...` 循环直接遍历，那么你需要实现一组特殊的 迭代器接口方法：

- `_iter_init(iter: Array) -> bool`

- `_iter_next(iter: Array) -> bool`

- `_iter_get(iter: Variant) -> Variant`

实现了它们之后，你的对象就可以像内置数组、字典一样愉快地参与循环

## 迭代的工作原理

1. 初始化阶段

    当循环开始时，`for` 会调用 `_iter_init(Array)` 来设置迭代的初始状态，并决定是否进入循环。

2. 每次循环推进
   
    每轮循环结束前，`for` 会调用 `_iter_next(Array)` 来尝试推进到下一个元素，如果返回 `false`，循环就会结束。

3. 获取当前值
   
    在每次循环内部，`for` 会调用 `_iter_get(Variant)` 获取当前迭代变量的值（这就是你在循环体里能拿到的变量值）。

## 接口方法说明

`_iter_init(iter: Array) -> bool`

- 用于设置迭代器的初始状态。

- 参数 `iter` 是一个单元素数组（GDScript 没有引用参数，所以用数组包装来传状态）。

- 返回 `true` 表示有元素可供迭代，返回 `false` 则直接结束循环。

例子：
```gdscript
func _iter_init(iter: Array) -> bool:
    if _arr.is_empty():
        return false
    _iter_index = 0
    iter[0] = _arr[0]
    return true
```

---

`_iter_next(iter: Array) -> bool`

- 推进到下一个元素，并更新迭代状态。

- 返回 true 表示还有元素可用，返回 false 表示结束。

例子：
```gdscript
func _iter_next(iter: Array) -> bool:
    _iter_index += 1
    if _iter_index >= _arr.size():
        return false
    iter[0] = _arr[_iter_index]
    return true
```

---

`_iter_get(iter: Variant) -> Variant`

- 根据当前迭代状态返回实际的值。

- 注意：这里 `iter` 是只读的 `Variant`，所以不能直接修改它的内容。

## 使用示例

使用我们文档最开始的`StaticArray`实现的迭代器：

```gdscript
var arr = StaticArray.new([1, 2, 3])
for x in arr:
    print(x)  # 输出 1, 2, 3
```