Like a typical interface, but is only allowed to have one abstract method. Designed to be used w/ lambda functions. Allowed to have other concrete methods as well.

Optional @FunctionalInterface argument.

Can have default methods and static methods, too.

There is a `java.util.function` package. Common ones include:
- `Function<T, R>`
- `Predicate<T>`
- `Consumer<T>`
- And more

## Examples
---
```
@FunctionalInterface
interface MathOperation {
	int operation(int a, int b);
}
```