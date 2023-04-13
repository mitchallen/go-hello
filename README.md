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

## To run remotely

* Push the build as a public repo to your github account

* Switch to a non-project directory to make sure things aren't running locally

** Replace **mitchallen** with **your github username**

```sh
go run github.com/mitchallen/go-hello@latest
```

It takes a minute to download and cache the package, but it should run.

You should see something like this:

```sh
go: downloading github.com/mitchallen/go-hello v0.0.0-20230413125123-316952b1a38d
hello world
```

Next time it should go faster, unless the version changed and it needs to update your local cache again.  You won't see the download again if the version hasn't changed.  You will just see the output:

```sh
hello world
```

## About caching

If you disconnect wifi, you won't be able to run the app remotely, even if it's cached.

Turn off wifi and you'll see something like this:

```sh
go run github.com/mitchallen/go-hello@latest
go: github.com/mitchallen/go-hello@latest: module github.com/mitchallen/go-hello: Get "https://proxy.golang.org/github.com/mitchallen/go-hello/@v/list": dial tcp: lookup proxy.golang.org: no such host
```





