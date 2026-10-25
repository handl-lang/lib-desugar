# How-to guides

Task recipes. Each assumes sibling checkouts of this repo and of the platform
repos it patches.

## Change a desugaring

Edit the transform definitions and rerun `plugin-lib-handl`'s tests; the engine needs no change, and the diff shows the rule that moved.

## Debug a surprising expansion

Run the pass alone and diff the AST before/after — the rewritten arena names the rule that fired.
