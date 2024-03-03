# Basic Project Layout

This is an outline to create and deploy a new golang based project.

## Overview

Currently this is a skeleton of subdirectories based on a reference package example.



## Go Directories

### `/cmd`

Main applications for this project.

### `/internal`

Private application and library code.

### `/pkg`

Library code that's ok to use by external applications.

### `/vendor`

Application dependencies.


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

### `/deploy`

IaaS, PaaS, system and container orchestration deployment configurations and templates (docker-compose, kubernetes/helm, terraform).

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

* [GoDoc](http://godoc.org) - It will provide online version of your GoDoc generated documentation.

    [![Go Doc](https://img.shields.io/badge/godoc-reference-blue.svg?style=flat-square)](http://godoc.org/github.com/nater0000/golang-pkg)

* [Pkg.go.dev](https://pkg.go.dev) - Pkg.go.dev is a new destination for Go discovery & docs.

	[![Go Reference](https://pkg.go.dev/badge/github.com/nater0000/golang-pkg.svg)](https://pkg.go.dev/github.com/nater0000/golang-pkg)

* Release - It will show the latest release number for your project.
    [![Release](https://img.shields.io/github/release/golang-standards/project-layout.svg?style=flat-square)](https://github.com/nater0000/golang-pkg/releases/latest)

## Notes

Project layout info see:
	[`Go Project Layout`](https://medium.com/golang-learn/go-project-layout-e5213cdcfaa2) for additional background information.
