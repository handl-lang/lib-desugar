# lib-desugar

The `desugar` transform-pass source, embedded by `plugin-lib-handl`.

## What it is

This repo carries the **desugar pass as handl data**: the `TransformDef`s the
runtime applies to surface syntax before evaluation. It is not a library a user
imports — `plugin-lib-handl` embeds it and hands the rules to
`engine-transform-rewrite`, so the pass can change without a runtime rebuild.

## Modules
- `src/index.hnl` — the transform definitions (the pass source)
- `src/lib.rs` — the embedding shim that exposes the source to the plugin


## Start here

- **Reference** — [public API](/lib-desugar/reference/)
- **How-to** — [task recipes](/lib-desugar/how-to/)
- **Explanation** — [design and rationale](/lib-desugar/explanation/)

No tutorials: this repo is a building block used from Rust. End-to-end
walkthroughs live with the product that composes it — see the
[Handl platform](/handl/).
