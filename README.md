# seaport-types

[![npm][npm-badge]][npm-link]

Structs, enums, interfaces, errors, and constants for [Seaport][seaport] 1.6. [seaport-core][seaport-core] compiles them into the deployed Seaport contract, and other Seaport repos and integrations import them.

The source in `src/` matches the deployed Seaport 1.6 bytecode and does not change.

## Install

With npm:

```bash
npm install seaport-types
```

Then import from `seaport-types/src/...`.

As a Foundry submodule:

```bash
forge install ProjectOpenSea/seaport-types
```

Then add the remapping `seaport-types/=lib/seaport-types/`.

## Development

Install [Foundry](https://getfoundry.sh) v1.9.0, then:

```bash
forge build
scripts/install-tools.sh   # once: pinned lint tools into .tools/bin
scripts/lint.sh check      # or fix
.tools/bin/lefthook install  # optional pre-commit hook
```

`scripts/install-tools.sh` downloads each tool from its GitHub release and checks it against a pinned SHA-256, so linting needs nothing from npm.

## Related repositories

- [seaport][seaport]: tests, docs, and the deployed `Seaport` wrapper
- [seaport-core][seaport-core]: the core Seaport 1.6 contracts
- [seaport-js][seaport-js]: TypeScript library for Seaport
- [seaport-sol][seaport-sol]: Solidity helpers for building Seaport orders in Forge scripts and tests

[seaport]: https://github.com/ProjectOpenSea/seaport
[seaport-core]: https://github.com/ProjectOpenSea/seaport-core
[seaport-js]: https://github.com/ProjectOpenSea/seaport-js
[seaport-sol]: https://github.com/ProjectOpenSea/seaport-sol
[npm-badge]: https://img.shields.io/npm/v/seaport-types?color=red
[npm-link]: https://www.npmjs.com/package/seaport-types
