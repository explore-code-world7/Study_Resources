# =
* 使用 = 将一个对象赋值给一个变量时，实际上是将该对象的引用（而不是对象本身）赋给变量。
* 对b 的修改也会影响到 对a的修改，因为b,a引用同一个对象。
* copy()则复制了一个新的对象。
## case
```python
a=[10,2]
b=a
a[1]=5
b
```
* 但对a的重新赋值，并不会影响到b

# list comprehension
使用列表推导式（list comprehension）构建列表通常比在 `for` 循环中逐个添加元素的方式更高效。这是因为列表推导式在内部实现上是优化过的，能够减少 Python 的函数调用开销和循环的开销。

## 性能比较
1. 列表推导式：
   - 列表推导式在创建列表时会在内存中一次性分配所需的空间，这样可以减少内存的重新分配次数。
   - 由于它是用 C 语言实现的，执行速度通常比 Python 的 `for` 循环快。

2. `for` 循环：
   - 在 `for` 循环中，每次添加元素时，Python 可能需要多次重新分配内存，尤其是在列表增长时，这会导致性能下降。
   - `for` 循环的语法相对较长，且每次迭代都涉及到 Python 的函数调用。

# @classmethod
在 Python 中，`@classmethod` 是一个装饰器，用于定义类方法。类方法的第一个参数是类本身（通常命名为 `cls`），而不是实例（通常命名为 `self`）。这使得类方法可以访问类的属性和方法，而不需要实例化该类。

## 主要作用

1. **访问类属性**: 类方法可以访问和修改类的属性，而不需要创建类的实例。

2. **工厂方法**: 类方法常用于定义工厂方法，这些方法可以根据不同的输入参数返回类的实例。

3. **与实例无关**: 类方法可以在没有实例的情况下被调用，这使得它们在某些情况下比实例方法更方便。

## 示例

以下是一个使用 `@classmethod` 的示例：

```python
class MyClass:
    class_variable = 0

    def __init__(self, value):
        self.instance_variable = value

    @classmethod
    def increment_class_variable(cls):
        cls.class_variable += 1

    @classmethod
    def create_instance(cls, value):
        return cls(value)

# 使用类方法访问和修改类变量
MyClass.increment_class_variable()
print(MyClass.class_variable)  # 输出: 1

# 使用类方法创建实例
instance = MyClass.create_instance(10)
print(instance.instance_variable)  # 输出: 10
```

## 解释

- `increment_class_variable` 是一个类方法，它通过 `cls` 参数访问和修改类变量 `class_variable`。
- `create_instance` 是一个工厂方法，它使用类方法创建并返回 `MyClass` 的实例。

## 总结

`@classmethod` 使得你可以在类级别上定义方法，这些方法可以访问类的属性和方法，而不需要实例化类。它在需要访问类状态或创建类实例时非常有用。
