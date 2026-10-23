Method overloading is done when there are two methods inside the same class with the same name. The methods must have different parameters, allowing you to call the method with either set of parameters. The return types for the methods can be the same or different, and the access can be anything. Method overloading differs from [[Method Overriding|method overriding]] in that the methods are in the same class, not in a sub/superclass.
## Example
---
Let's say you have a class named `Paper` and you want to add a `draw` method. You want to be able to draw with a pen or a pencil.