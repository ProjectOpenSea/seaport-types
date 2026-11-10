# seaport-types

Structs, enums, interfaces, errors, and constants for Seaport 1.6. [seaport-core](https://github.com/ProjectOpenSea/seaport-core) and [seaport](https://github.com/ProjectOpenSea/seaport) import them, and they are published to npm as `seaport-types`.

## Rule

Never change a `.sol` file in `src/`, not even whitespace. seaport-core compiles this source into the deployed Seaport 1.6 bytecode, and `scripts/frozen-contracts.sha256` fails CI if any of it changes. `foundry.toml` and `lefthook.yml` keep `forge fmt` and `forge lint` off `src/`.

## Commands

Foundry v1.9.0.

```bash
forge build
scripts/install-tools.sh   # pinned Biome, taplo, lefthook, shellcheck, shfmt, actionlint
scripts/lint.sh check      # or fix
```

## Publishing

Creating a GitHub release runs `.github/workflows/publish.yml`, which publishes the package to npm with provenance. Bump `version` in `package.json` first. The package has no dependencies; keep it that way.
