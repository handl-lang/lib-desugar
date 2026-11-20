# lib-desugar

The `desugar` transform pass source, embedded by `plugin-lib-handl`.

## Layout

```text
src/                     the .hnl sources plus the const crate
pkg.hnl                  package manifest
scripts/hnl-gate.sh      the gate
ci.sh                    bupha entry
```

## Gate

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.

## Documentation

<https://handl-lang.github.io/docs/lib-desugar/>
