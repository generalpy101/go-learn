## Go Variables

- Variables are essential part of a high level programming language.
- A variable is like a container/box which stores some data.
- It is basically an alias for a location in memory which is also more readable for us humans.
- Since variables are aliases for memory locations, they are basically names which must be human readable.
- In Go the convention for those "names" is to use camelCase. In camelCase we start with lowercase word and then if we want to add a new word, we start with upper case. Note that variable names cannot have spaces so new word and old word cannot have spaces. Word camelCase is comprised of two words, camel and case and is a valid, conventional variable name.
- In Go variables must be declared before we can use and assign them.
- **Declaration** of variable is a way for us to tell computer that we want a box in memory, reserve it for us. **Assignment** is a way for us to tell computer that we want to put some data into that box which is residing in memory.


### Go variables syntax

There are various ways to declare and use variables in Go.

```go
// Declaring a variable
var variableName
var variableName int

// Assigning variable a value
variableName = 10 // variable must exist

// Declaration and assignment at same statement
var variableName = 10
var variableName int = 10

// Special declaration and assignment operator
variableName := 10  // new variable is created

// Compound variable declaration
var a,b,c = 10,1.3,"root" // 3 different datatypes
a,b,c := 10,1.3,"root"

// Batch variable declaration with data type 
var (
    a int = 10
    b = 1.3
    x string = "root"
)

// Comman, ok 
a,err := 10, "root"
b,err := 11, "root not defined"

// Constants 
const ConstantName = 10
```
`var` is a reserved keyword in Go which is used to declare variables. We can optionally add datatype after variable name. If datatype is written, variable must be assigned same type of data or else error will be raised. If datatype is not provided, variable datatype will be same as first value assigned to it. 

We can assign variables n numbers of times provided that datatype is correct.

Variables can be assigned to other variables.

```go
a := 10
b := a
a = 5
// a = 5, b = 10
```

When reassigning, a copy of variable is created so changing value of real variable (a) doesn't changes copied variable(b).

When data type is provided but values are not assigned, defaults are assigned to variables which are 0 for numbers, "" for strings and `nil` for other data types.

`:=` is a special operator which is used to create and assign variable at the same time without use of `var` keyword. Since it is less code to write, it is used extensively.

We can declare and assign multiple variables in a single line using comma(,) or using block declaration.

Note that a variable cannot be re declared in the current scope i.e variables are unique in their scope. Scope is the boundary till that the variable is valid.

```go
a := 10
var a int // error
a = 11 // valid as this is just re assignment
a := 11 // error
```

One exception to this rule is Comma, ok statement. In this statement, we can re declare a variable when compoundly done with another variable.

```go 
a,err := 10, "root"
b,err := 11, "root not defined"
```

Above code block is example of Comma, ok. Here err is redeclared every time, also supporting data type change.

There are also constants in Go. We can use `const` keyword to declare constants. Constants cannot be reassigned.