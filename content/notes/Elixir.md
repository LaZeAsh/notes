---
title: "Elixir"
---

Elixir is a dynamic, functional programming language designed for building scalable and maintainable applications, particularly known for its use in concurrent and distributed systems

## Elixir Quirks

A list of things about elixir that are unique compared to other languages

- Whenever you use `/` symbol in elixir it returns a float value rather than an integer
- After invoking `iex` you can use the command `h [module_name].[function_name]/[# of parameters]` to find documentation on that individual function
- ONLY `nil` and `false` are considered "falsy" values in elixir
	- Values like `0` and `""` are considered to be "truthy" values in elixir
- `Atom` - An atom is a constant whose value is its own name. Some other languages call these symbols
	- `Atom Operations`:
		- :apple == :apple 
			- Output: true
		- :apple == :orange
			- Output: false
		- true == :true
			- Output: true
		- is_atom(false)
			- Output: true
		- is_boolean(:false)
			- Output: true
- Booleans true and false are also atoms
- To concatenate strings in elixir you use the `<>` operation
	- "hello " <> "world!"
		- Output: "hello world!"
- Elixir also allows string interpolation
	- string = "world"
	- "hello #{string}!"
		- Output: "hello world!"
- Integer and floats compare the same if they have the same value
	- 1 == 1.0
		- Output: true
- 