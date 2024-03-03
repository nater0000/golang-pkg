# Standard Go Project Layout

Translations:

* 

## Overview

This is a basic layout for Go application projects.



## Go Directories

### `/cmd`

Main applications for this project.

### `/internal`

Private application and library code.

### `/pkg`

Library code that's ok to use by external applications (e.g., `/pkg/mypubliclib`). Other projects will import these libraries expecting them to work, so think twice before you put something here :-) Note that the `internal` directory is a better way to ensure your private packages are not importable because it's enforced by Go. The `/pkg` directory is still a good way to explicitly communicate that the code in that directory is safe for use by others. The [`I'll take pkg over internal`](https://travisjeffery.com/b/2019/11/i-ll-take-pkg-over-internal/) blog post by Travis Jeffery provides a good overview of the `pkg` and `internal` directories and when it might make sense to use them.

### `/vendor`

Application dependencies (managed manually or by your favorite dependency management tool like the new built-in [`Go Modules`](https://github.com/golang/go/wiki/Modules) feature). The `go mod vendor` command will create the `/vendor` directory for you. Note that you might need to add the `-mod=vendor` flag to your `go build` command if you are not using Go 1.14 where it's on by default.


## Service Application Directories

### `/api`

API

## Web Application Directories

### `/web`

Web application specific components: static web assets, server side templates and SPAs.

## Common Application Directories

### `/configs`

Configuration file templates or default configs.

### `/init`

System init (systemd, upstart, sysv) and process manager/supervisor (runit, supervisord) configs.

### `/scripts`

Scripts to perform various build, install, analysis, etc operations.

### `/build`

Packaging and Continuous Integration.

### `/deployments`

IaaS, PaaS, system and container orchestration deployment configurations and templates (docker-compose, kubernetes/helm, terraform). Note that in some repos (especially apps deployed with kubernetes) this directory is called `/deploy`.

### `/test`

Additional external test apps and test data.

## Other Directories

### `/docs`

Design and user documents.

### `/tools`

Supporting tools for this project.

### `/examples`

Examples.

### `/third_party`

External helper tools, forked code and other 3rd party utilities.

### `/githooks`

Git hooks.

### `/assets`

Other assets.

### `/website`

Website data

## Badges

* [Go Report Card](https://goreportcard.com/) - It will scan your code with `gofmt`, `go vet`, `gocyclo`, `golint`, `ineffassign`, `license` and `misspell`.

    [![Go Report Card](https://goreportcard.com/badge/github.com/golang-standards/project-layout?style=flat-square)](https://goreportcard.com/report/github.com/nater0000/golang-pkg)

* ~~[GoDoc](http://godoc.org) - It will provide online version of your GoDoc generated documentation.

    [![Go Doc](https://img.shields.io/badge/godoc-reference-blue.svg?style=flat-square)](http://godoc.org/github.com/nater0000/golang-pkg)

* [Pkg.go.dev](https://pkg.go.dev) - Pkg.go.dev is a new destination for Go discovery & docs.
	[![Go Reference](https://pkg.go.dev/badge/github.com/nater0000/golang-pkg.svg)](https://pkg.go.dev/github.com/nater0000/golang-pkg)

* Release - It will show the latest release number for your project.
    [![Release](https://img.shields.io/github/release/golang-standards/project-layout.svg?style=flat-square)](https://github.com/nater0000/golang-pkg/releases/latest)

## Notes

Project layout info see:
	[`Go Project Layout`](https://medium.com/golang-learn/go-project-layout-e5213cdcfaa2) for additional background information.
