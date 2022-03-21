<p align="center"><a href="#readme"><img src="https://gh.kaos.st/godoc-action.svg"/></a></p>

<br/>

Action for invoking documentation generation on [pkg.go.dev](https://pkg.go.dev).

### Usage

Create file `.github/workflows/godoc.yml`.

Add next code to it:

```yml
name: GoDoc

on:
  create

jobs:
  GoDoc:
    name: Generate docs
    runs-on: ubuntu-latest

    steps:
      - name: Trigger GoSumDB and PkgGoDev
        uses: essentialkaos/godoc-action@v1

```

You can generate documentation for sources on custom domains. For example for `gopkg.in`:

```yml
name: GoDoc

on:
  create

jobs:
  GoDoc:
    name: Generate docs
    runs-on: ubuntu-latest

    steps:
      - name: Trigger GoSumDB and PkgGoDev
        uses: essentialkaos/godoc-action@v1
        with:
          domain: gopkg.in

```

### License

[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)

<p align="center"><a href="https://essentialkaos.com"><img src="https://gh.kaos.st/ekgh.svg"/></a></p>
