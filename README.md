# lib-desugar

The `desugar` transform pass source, embedded by `plugin-lib-handl`.

Part of the `handl-lang` org split (ADR-0128). History is a `git subtree
split` of `host/handl-packages/handl-packages/desugar/`.

## Layout

```text
src/        the .hnl sources
pkg.hnl     dependencies, when any: `{ deps: { <name>: "branch:<ref>" } }`
```

## Gate

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## Documentation

Published site (Diátaxis): <https://handl-lang.github.io/docs/lib-desugar/>

- [Reference](https://handl-lang.github.io/docs/lib-desugar/reference/) — public API surface
- [How-to](https://handl-lang.github.io/docs/lib-desugar/how-to/) — task recipes
- [Explanation](https://handl-lang.github.io/docs/lib-desugar/explanation/) — design and rationale

Decision records live on the `project` branch under `project/adrs/`.

## License

MIT.
