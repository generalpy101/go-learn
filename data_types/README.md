## Data Types 

- All data in computers is represented by binary digits(1s and 0s). These numbers don't make much sense to us humans.
- Data types are way through which a program can interpret these binary numbers.
- There are different data types like numbeers(1,2,1.3), strings("abc") etc.
- Go is a statically typed language so data types must be provided by programmers.
- Also Go uses type inference to automatically determine type of data used but we still have to provide types in specific circumstances.
- If we provide data type in Go, that type must be used or else type error is raised by the compiler.


### Primitive data types 

- All primitive data types in Go are numeric i.e streams of bytes.
- Due to this there can be error sometimes when taking user input or manually inputting byte stream.

__Some basic Go datatypes are :-__


<img src="../data_types/media/images/signed-integer-types.png" width="1200" />


<img src="../data_types/media/images/unsigned-integer-types.png" width="1200" />


<img src="../data_types/media/images/other-data-types.png" width="1200" />


### Type Aliases

- Like C `typedef` we can use type aliases in Go.
- These aliases perform same functionality as the original data type but have a different name.
- We can also type alias type aliases.


Syntax for type aliasing is :

```go
type newName oldName
type UserId int
type Speed float32
type Velocity Speed
```

Here Both old an new type will coexist.

To convert types to type alias type we have to use parentheses.

Eg : 

```go
UserId(10)
Speed(13.32)
```