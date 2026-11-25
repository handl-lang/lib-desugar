# lib-desugar

The `desugar` transform pass **source**, vendored by
`plugin-lib-handl` — the `.hnl` that implements the desugar pass the
handl compiler runs.

## Layout

| path | role |
| --- | --- |
| `src/index.hnl` | the pass source |
| `docs/` | docs |
| `pkg.hnl` | manifest — `modules: ["desugar"]` |
| `scripts/hnl-gate.sh` | `.hnl` gate |
| `workflows/gate.yaml` | CI — shared `handl-gates` campaign |

## Contract

- Pure `.hnl` only — consumers copy `pkg.hnl` + `src/**/*.hnl` via
  `handl-pkg-vendor` into `OUT_DIR` and embed with `include_str!`
  (`plugin-lib-handl` does this; the `handl-lib-desugar` crate shim is
  deleted).
- This is compiler-pass source, not a library API — changes affect
  desugaring semantics downstream.

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
