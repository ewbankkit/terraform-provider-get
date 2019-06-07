Terraform `go-getter` Provider
==============================

Requirements
------------

-	[Terraform](https://www.terraform.io/downloads.html) 0.10+
-	[Go](https://golang.org/doc/install) 1.12 (to build the provider plugin)

Building The Provider
---------------------

*Note:* This project uses [Go Modules](https://blog.golang.org/using-go-modules) making it safe to work with it outside of your existing [GOPATH](http://golang.org/doc/code.html#GOPATH). The instructions that follow assume a directory in your home directory outside of the standard GOPATH (i.e `$HOME/development/EvilSuperstars/`).


Clone repository to: `$HOME/development/EvilSuperstars/`

```sh
$ mkdir -p $HOME/development/EvilSuperstars/; cd $HOME/development/EvilSuperstars/
$ git clone git@github.com:EvilSuperstars/terraform-provider-get
```

Enter the provider directory and build the provider

```sh
$ cd $HOME/development/EvilSuperstars/terraform-provider-get
$ make build
```

Run acceptance tests

```sh
$ cd $HOME/development/EvilSuperstars/terraform-provider-get
$ make testacc TEST=./get/ TESTARGS='-run=TestDataSource_'
```

Using The Provider
------------------

See the [documentation](using.md) to get started using the [go-getter](https://github.com/EvilSuperstars/terraform-provider-get) provider.
