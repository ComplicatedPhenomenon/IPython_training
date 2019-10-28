> In compiled languages, a variable is a memory space that is able to capture the value of the type. In Python, a variable is a name (captured internally as a string) bound to the reference variable that holds the reference value to the target object. The name of the variable is the key in the internal dictionary, the value part of that dictionary item stores the reference value to the target.


> There are no variables in Python. The key to understanding parameter passing is to stop thinking about "variables". There are names and objects in Python and together they appear like variables, but it is useful to always distinguish the three.

* Python has names and objects.
* Assignment binds a name to an object.
* Passing an argument into a function also binds a name (the parameter name of the function) to an object.


# Data structure
## How `list` is implemented?

```c
typedef struct {
    # 列表对象引用计数
    int ob_refcnt;  
    # 列表类型对象      
    struct _typeobject *ob_type;
    # 列表元素的长度
    int ob_size; /* Number of items in variable part */
    # 真正存放列表元素容器的指针，list[0] 就是 ob_item[0]
    PyObject **ob_item;
    # 当前列表可容纳的元素大小
    Py_ssize_t allocated;
} PyListObject;
```

## How `set` is implemented?


## How `dict` is implemented?


## How `balanced binary search tree` is implemented?


## How `black red tree` is implemented?

## `list` vs `tuple`
https://foofish.net/list-different-with-tuple.html

一个对象在其生命周期内，如果保持不变，就是 hashable（可哈希的）。

在Python中：

list、set和dictionary 都是可改变的，比如可以通过list.append()，set.remove()，dict['key'] = value对其进行修改，所以它们都是不可哈希的；

而tuple和string是不可变的，只可以做复制或者切片等操作，所以它们就是可哈希的。

# reference
https://foofish.net
