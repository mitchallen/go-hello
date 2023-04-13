## Usage

```sh
go run go-hello.go
```

### Build

Note that these are command line instruction for Mac / Linux OS:

```sh
go build go-hello.go
ls
   go-hello    go-hello.go
```

Run binary that you just built:

```
./go-hello
```

## To turn it into a proper package

** Replace **mitchallen** with **your github username**

```sh
go mod init github.com/mitchallen/go-hello
go mod tidy
```

This will create a new go.mod file in your project root:

```sh
ls go.mod
cat go.mod
```

