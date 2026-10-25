# Explanation

## Why this crate exists

Desugaring used to live inside the runtime, so changing it meant changing
Rust. Moving the pass source into its own repo (ADR-0128 split) makes the pass
inspectable and versionable, and keeps the runtime a consumer of passes rather
than their owner.

## Where it sits

This crate belongs to the `engine-*` family. Plugins, kits and hosts reach it
through the kit's operation slot, so the engine can be swapped without touching a
language definition.

See the [reference](/lib-desugar/reference/) for the API and the
[how-to guides](/lib-desugar/how-to/) for tasks.
