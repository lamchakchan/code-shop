# Programmatic builder for LLB

## Overview
An example to understand how to dynamically create a LLB for the frontend with build kit.

## Dumping out the LLB

```shell
go run builder.go | 
 buildctl debug dump-llb |
 jq .
```

## Building a Docker image and pushing to a registry

```shell
$ go run builder.go | buildctl build --local context=. --output type=image,name=docker.io/lamchakchan/custom-llb-test,push=true
```