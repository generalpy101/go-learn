## Packages and Modules


### Packages


- Packages are Go's way of organizing code.
- Go programs are generally written in form of one or more packages. We can import packages.
- Third party packages can also be used from Go registry.
- Packages are generally meant to be focused and must do a single task like argument parsing, http request handling etc.
  
To use packages the syntax is : 

```go
import "packageName"

import (
    "package1"
    "namespace/package2"
)
```

As shown above, we can batch multiple packages and can also arrange them in namespaces for easy categorization.

When we import packages in above mentioned ways, we have to use package name before accessing its contents but we can use a different syntax to avoid that.

We can also rename package when importing.

Updated syntax is :

```go
import (
    . "packageName"
    newName "packageName"
)
```

### Modules


- Modules are collection of packages.
- A Go module is created by have `go.mod` file in its root directory.
- The `go.mod` file contains different information about the module like version, name, dependencies etc.
- All Go projects have a `go.mod` file.


__Example go.mod file__

```go
module "namespace/moduleName"

go goVersion

require (
    dependencies...
)
```