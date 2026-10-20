---

---
Abstraction is the generalization of a concept. In programming, we use abstraction to hide details and implementations that we do not need to know or do not care about. For example, when we use `System.out.println();`, the details about how exactly Java is outputting something to the console is hidden away. Abstraction makes our lives a lot simpler in programming.
## Restricted Abstractions
---
In data structures, restricted abstractions refers to abstract data types (ADT) that limits the way data can be accessed and manipulated. 
### With a stack
In a [[Stack|stack]], we can only manipulate the element on the top of the stack. You can only do three things in a pure stack:
- Push: Add a new element on top of the stack
- Pop: Remove the top element of the stack
- Peek/top: See what the top element of the stack is
Basically, all the other data in the stack are abstracted away until we can access them. The stack implements restricted abstractions by limiting what we can do to the stack.
### With a queue
Can only put a new element at the end, and take out elements from the beginning.
### With a dequeue
Restricted ops:
