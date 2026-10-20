## Stack Memory / Call Stack
---
- Hold local vars and function calls
- Uses last in first out (LIFO)
The call stack is an abstract data type. It allows insertions or removals only from one end, kind of like stacking objects in the real world. You have to take the top object off the stack first.
Variables destroyed when a frame is removed.
+++ REVIEW
## Heap Memory
----
Holds all dynamically allocated objs, added when using the `new` keyword. The heap is much larger than the stack. Access is slower because memory is managed flexibly. Each object in heap memory has a memory address referenced by variables in the stack or in other objects. Java has its own garbage collection.
Heap can run out of memory quickly, and trying to instantiate with no more space will cause a crash. Here is an example of wasted space:
```

```
+++ REVIEW
### Garbage collection:
Reclaims heap memory
Periodically performed
### String Pool
A special area in the heap, which stores string literals. This helps with memory optimization by reusing identical existing strings.
Strings are immutable, so every time we edit them, we are creating a new string literal in the string pool. If we are frequently changing what looks like the same string, we should instead use the mutable type `StringBuffer`

## Static Area (Method Area)
Used to store:
- Class level data like static vars, consts, and method definitions
- Class metadata like class names, methods, and fields


