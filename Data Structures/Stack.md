A stack is a data structure that follows a last in, first out principle (LIFO). When we add elements to a stack, the last element we add is the only one we can control, unless we remove the top element and access the one beneath it.
![[Pasted image 20261020155219.png|327]]
We can think of a stack as a literal stack of something, like plates. We can add, remove, and work with a plate on top of the stack. But, to access the second plate from the top, we must first remove the top plate.
A stack usually implements three methods:
- Push: Add an element on top
- Pop: Remove the top element
- Peek/top: View the top element
All of these methods can work in [[Complexity Analysis|O(1) complexity]], since we are only working with one element and not iterating through an entire list.
The stack implements [[Abstraction#Restricted Abstractions|restricted abstraction]], since we can only do certain operations on the data.