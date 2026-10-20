An initialization block is a block of code, contained by brackets `{}`, that goes at the top of a class. This block of code will always run BEFORE a constructor or any other piece of code inside a class. It is typically use to initialize instance or static variables, hence its name. Using initialization blocks, we can put complicated logic inside the block of code that might use other data to initialize variables. Or, instead of repeating the same stuff in a constructor that never changes across instances, we can just put it in the block.
There are two kinds of initialization blocks, instance and static blocks.
## Instance Initialization Block
---
Below is an example of an instance initialization block:
```
class Examp {
	private int x;
	
	// Init block here vvv
	{
		x = 20;
	}
	// End init block
	
	public Examp() {
		System.out.println(x);
	}
}
```
The initialization block sets the variable `x` to `20`. Then, the constructor runs, printing `20`. The block will run every time a new instance of the `Examp` class is created, since it does NOT have the keyword static in front of it.
## Static Initialization Block
---
Here is an example of a static initialization block:
```
class Foo {
	public static int bar;
	
	// Init block here vvv
	static {
		bar = 1000;
	}
	// End init block
	
	public Foo() {
		System.out.println(bar);
	}
	
	public int getBar() {
		return bar;
	}
}
```
The only difference is the keyword `static` in front of the first brace.
Static initialization blocks will only run ONCE per run of the program.
It ONLY runs the first time the class is ever used, whether it is through instance creation or method calling. The first time `Foo` is mentioned, the code will run. So anytime we try to touch `bar`, it will ALWAYS be 1000.
Examples of accessing Foo:
```
Foo f = new Foo();
System.out.println(Foo.bar);
System.out.println(Foo.getBar());
```