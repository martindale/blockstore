# Blockstore: A Key-Value Store on Bitcoin

[![PyPI](https://img.shields.io/pypi/v/blockstore.svg)](https://pypi.python.org/pypi/blockstore/)
[![PyPI](https://img.shields.io/pypi/dm/blockstore.svg)](https://pypi.python.org/pypi/blockstore/)
[![PyPI](https://img.shields.io/pypi/l/blockstore.svg)](https://github.com/blockstack/blockstore/blob/master/LICENSE)

Blockstore is a generic key-value store on Bitcoin. You can use it register globally unique names, associate data with those names, and transfer them between Bitcoin addresses.

Then, you or anyone can perform lookups on those names and securely obtain the data associated with them.

Blockstore uses the Bitcoin blockchain for storing name operations and data hashes, and the Kademlia distributed hash table for storing the full data files.

## Installation

The fastest way to get started with blockstore is to use a docker image:

```
docker run -it --entrypoint=/bin/bash blockstack/blockstored
```

The docker image comes pre-populated with a snapshot that was processed till a recent block and you won't have to process all the blocks yourself (takes time). Alternatively, you can install a version on your machine directly:

```
pip install blockstore
```

## Getting Started

Start blockstored and index the blockchain:

```
$ blockstored start
```

Then, perform name lookups:

```
$ blockstore-cli lookup swiftonsecurity
{
    "data": "{\"name\":{\"formatted\": \"Taylor Swift\"}}"
}
```

Next, learn how to register names of your own, as well as transfer them and associate data with them:

[Full usage docs](../../wiki/Usage)

## Design

[Design decisions](../../wiki/Design-Decisions)

[Protocol details](../../wiki/Protocol-Details)

[Definitions](../../wiki/Definitions)

[FAQ](../../wiki/FAQ)

## Contributions

The best way to contribute is to:

1. decide what changes you'd like to make (you can find inspiration in the tab of issues)
1. fork the repo
1. make your changes
1. submit a pull request

[Code contributors](../../graphs/contributors)

[Full contributor list](../../wiki/Contributors)

## License

[Released under the MIT License](LICENSE)

Copyright 2015, openname.org
