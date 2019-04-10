# pbparser

Package in Go for parsing Google Protocol Buffers.
Not support to work on Windows.

## Install

```console
go get -u github.com/sonatard/pbparser
```

## Usage

```go
package main

import (
	"fmt"

	"github.com/sonatard/pbparser"
)

func main() {
	file := "sample.proto"
	imports := []string{"./", "PROTO_DIR"}
	fd, err := pbparser.ParseFile(file, imports...)
	if err != nil {
		// error handling
	}

	fmt.Printf("%v\n", fd)
}
```

