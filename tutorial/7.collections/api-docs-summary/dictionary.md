# 字典方法 API文档摘要

> 对于类型化字典，部分方法的参数类型应根据字典键值类型而变化，**GDScript不会在传参时进行类型检查，类型不匹配时会造成预期外的情况**

# `void assign(dictionary: Dictionary)`

### **参数**

* `dictionary`：要拷贝内容的 Dictionary，可以是普通或类型化字典。

***

### **方法说明**

用传入的字典替换（进行浅拷贝）当前字典的内容。如果是类型化字典，会尝试进行必要的类型转换。



# `void clear()`

### **方法说明**

清空字典中的所有键值对，相当于让它变成一个新的空字典。



# `Dictionary duplicate(deep: bool = false) const`

### **参数**

* `deep`：是否进行深拷贝。为 `true`时会递归复制嵌套的 `Dictionary`和 `Array`。

***

### **方法说明**

返回该字典的副本，`deep`模式下嵌套的结构也会一起复制。

***

### **返回值**

一个新的 `Dictionary`，内容与当前字典相同。



# `bool erase(key: Variant)`

### **参数**

* `key`：要移除的键。

***

### **方法说明**

如果存在对应的键，则将该键及其值从字典中删除。

***

### **返回值**

一个布尔值，指示是否成功删除了键值对。



# `Variant find_key(value: Variant) const`

### **参数**

* `value`：要查找的值。

***

### **方法说明**

查找第一个关联的值等于`value`的键

***

### **返回值**

找到的键，如果没有找到则为`null`。



# `Variant get(key: Variant, default: Variant = null) const`

### **参数**

* `key`：要查找的键。

* `default`（可选）：如果没有找到该键时要返回的默认值。

***

### **方法说明**

返回 `key`对应的值，若键不存在则返回 `default`。

***

### **返回值**

对应的值或 `default`值。



# `Variant get_or_add(key: Variant, default: Variant = null)`

### **参数说明**

* `key`：要查找或添加的键。

* `default`（可选）：如果键不存在，将插入并返回该默认值。

***

### **方法说明**

如果 `key`已存在则返回它的值；否则插入`key : default`并返回`default`。

***

### **返回值**

键对应的值或插入的 `default`。



# `int get_typed_key_builtin() const`

### 方法说明

获取字典的键的类型（用 `Variant.Type` 的数字表示）。如果不是类型化的，就返回 `TYPE_NIL`

***

### 返回值

`Variant.Type`常量值，表示字典的键的类型



# `StringName get_typed_key_class_name() const`

### 方法说明

获取键的内置类名；如果键不是对象类型就返回空字符串。

***

### 返回值

唯一字符串形式的键的类型，如果不是对象类型则返回空字符串



# `Variant get_typed_key_script() const`

### 方法说明

获取键关联的脚本（Script）实例，没有则返回`null`

***

### 返回值

键所关联的脚本实例（`Script`类型），如果不存在则返回`null`



# `int get_typed_value_builtin() const`

### 方法说明

获取字典的值的类型（用 `Variant.Type` 的数字表示）。如果不是类型化的，就返回 `TYPE_NIL`

***

### 返回值

`Variant.Type`常量值，表示字典的值的类型



# `StringName get_typed_value_class_name() const`

### 方法说明

获取值的内置类名；如果值不是对象类型就返回空字符串。

***

### 返回值

唯一字符串形式的值的类型，如果不是对象类型则返回空字符串



# `Variant get_typed_value_script() const`

### 方法说明

获取值关联的脚本（Script）实例，没有则返回`null`

***

### 返回值

值所关联的脚本实例（`Script`类型），如果不存在则返回`null`



# `bool has(key: Variant) const`

### 参数

* `key`：要检测的键。

***

### 方法说明

如果该字典包含给定的键 `key`，则返回 `true`。只要键存在，即使对应的值为`null`，也返回 `true`。

在 GDScript 中，`has()` 等价于 `in` 运算符：

***

### 返回值

一个布尔值，指示给定的键是否存在于字典中

***

### 示例



# `bool has_all(keys: Array) const`

### 参数

* `keys`：包含多个键的数组。

***

### 方法说明

如果该字典包含 `keys`中的所有键，则返回 `true`。

***

### 返回值

一个布尔值，指示给定数组中的所有键是否全都存在于字典中

***

### 示例



# `int hash() const`

### 方法说明

返回一个 32 位整数，代表该字典内容的哈希值。

两个字典条目顺序不同哈希值也不同。**哈希相同不保证内容完全相同，但哈希不同的字典一定不相同。**

***

### 返回值

表示字典内容的 32 位哈希值。

***

### 示例



# `bool is_empty() const`

### 方法说明

判断字典是否为空（无任何条目）。

***

### 返回值

字典为空时返回 `true`，否则返回 `false`。



# `bool is_read_only() const`

### 方法说明

判断字典是否只读。

***

### 返回值

字典为只读时返回 `true`，否则返回 `false`。



# `bool is_same_typed(dictionary: Dictionary) const`

### 参数

* `dictionary`：另一个字典。

***

### 方法说明

判断当前字典与传入字典是否键和值的类型都相同。

***

### 返回值

类型相同返回 `true`，否则返回 `false`。



# `bool is_same_typed_key(dictionary: Dictionary) const`

### 参数

* `dictionary`：另一个字典。

***

### 方法说明

判断当前字典与传入字典的键的类型是否相同。

***

### 返回值

键类型相同返回 `true`，否则返回 `false`。

# `bool is_same_typed_value(dictionary: Dictionary) const`

### 参数

* `dictionary`：另一个字典。

***

### 方法说明

判断当前字典与传入字典的值的类型是否相同。

***

### 返回值

值类型相同返回 `true`，否则返回 `false`。

***

# `bool is_typed() const`

### 方法说明

判断该字典是否为类型化字典（键和值类型受限制）。

***

### 返回值

是类型化字典返回 `true`，否则 `false`。

***

# `bool is_typed_key() const`

### 方法说明

判断该字典的键是否有类型限制。

***

### 返回值

键有类型限制返回 `true`，否则 `false`。

***

# `bool is_typed_value() const`

### 方法说明

判断该字典的值是否有类型限制。

***

### 返回值

值有类型限制返回 `true`，否则 `false`。



# `Array keys() const`

### 方法说明

返回该字典中所有键的 `Array`。

***

### 返回值

包含所有键的 `Array`。



# `void make_read_only()`

### 方法说明

将该字典设置为只读，禁止进一步修改。注意，对嵌套内容（如嵌套字典）无效。



# `void merge(dictionary: Dictionary, overwrite: bool = false)`

### 参数

* `dictionary`：要合并进当前字典的另一个字典。

* `overwrite`（可选）：是否覆盖已有键（默认为 false）。

***

### 方法说明

将另一个字典的内容合并到当前字典中。默认不会覆盖重复键，除非 `overwrite`为 `true`。该方法不进行递归合并。

***

### 示例



# `Dictionary merged(dictionary: Dictionary, overwrite: bool = false) const`

### 参数

* `dictionary`：用于合并的新字典。

* `overwrite`（可选）：是否在遇到重复键时覆盖（默认为 `false`）。

***

### 方法说明

返回一个新的字典，包含当前字典与传入字典合并后的内容。与 `merge()` 不同，**该方法不修改原始字典，而是返回合并结果的新副本。**

***

### 返回值

合并后的 `Dictionary`副本。

***

### 示例



# `bool recursive_equal(dictionary: Dictionary, recursion_count: int) const`

### 参数

* `dictionary`：要进行比较的另一个字典。

* `recursion_count`：最大递归深度。

***

### 方法说明

判断两个字典是否结构与内容都一致，包括内部嵌套的 `Dictionary`和 `Array`，会进行递归比较。

***

### 返回值

若所有键值都相等则返回 `true`，否则返回 `false`。



# `bool set(key: Variant, value: Variant)`

### 参数

* `key`：要设置的键。

* `value`：对应的新值。

***

### 方法说明

将键对应的值设为给定值，相当于 `dict[key] = value`。

对于类型化字典，类型错误时不会报错

***

### 返回值

返回 `true`表示设置成功。



# `int size() const`

### 方法说明

返回该字典中当前的条目数量。

***

### 返回值

条目的数量（整数）。



# `void sort()`

### 方法说明

按键对字典原地排序，使转换为字符串或序列化时具有稳定顺序。适合用于有序输出或数据库存储。



# `Array values() const`

### 方法说明

返回该字典中所有值组成的数组。

***

### 返回值

一个 `Array`，包含字典的所有值。

