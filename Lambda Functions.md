AKA anonymous functions
No name, not bound to a class.
Very specific syntax. Can be hard to read.
Syntax example:
`(argument list) -> {body}`
- Arg list can be empty or not
- Arrow token is required
- Body is what you do, the function body

Params:
- No params
	- `() -> expression`
- One param
	- `param -> exp`
	- `(param) -> exp`
- Two or more
	- `(param, param) -> exp`
	- `(param, param) -> {exp block}`

Characteristics:
- Optional type declaration
- Optional parens around params
- Optional curly braces
- Optional return keyword
- Anonymous
- Concise
- Function
- Can be passed