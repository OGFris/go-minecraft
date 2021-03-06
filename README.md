# Library for Minecraft

[![Build Status](http://drone.kleister.tech/api/badges/kleister/go-minecraft/status.svg)](http://drone.kleister.tech/kleister/go-minecraft)
[![Stories in Ready](https://badge.waffle.io/kleister/kleister-api.svg?label=ready&title=Ready)](http://waffle.io/kleister/kleister-api)
[![Join the Matrix chat at https://matrix.to/#/#kleister:matrix.org](https://img.shields.io/badge/matrix-%23kleister%3Amatrix.org-7bc9a4.svg)](https://matrix.to/#/#kleister:matrix.org)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/e96f91f1bce14e049a3d3db93baa4683)](https://www.codacy.com/app/kleister/go-minecraft?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=kleister/go-minecraft&amp;utm_campaign=Badge_Grade)
[![Go Doc](https://godoc.org/github.com/kleister/go-minecraft?status.svg)](http://godoc.org/github.com/kleister/go-minecraft)
[![Go Report](http://goreportcard.com/badge/github.com/kleister/go-minecraft)](http://goreportcard.com/report/github.com/kleister/go-minecraft)

This repository will provides helpers related to Minecraft.


## Development

TBD


## Examples

### Fetch available Minecraft versions

[embedmd]:# (examples/versions/main.go go)
```go
package main

import (
	"log"

	"github.com/kleister/go-minecraft/version"
)

func main() {
	log.Println("Fetching Minecraft versions...")
	minecraft, err := version.FromDefault()

	if err != nil {
		log.Fatalf("%s", err)
	}

	for _, version := range minecraft.Releases {
		log.Printf("Minecraft v%s", version.ID)
	}
}
```


## Security

If you find a security issue please contact kleister@webhippie.de first.


## Contributing

Fork -> Patch -> Push -> Pull Request


## Authors

* [Thomas Boerger](https://github.com/tboerger)


## License

Apache-2.0


## Copyright

```
Copyright (c) 2018 Thomas Boerger <thomas@webhippie.de>
```
