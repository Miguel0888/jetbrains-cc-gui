# Fork branch strategy

This fork temporarily keeps two long-lived branches while the CoDriver skin pull request is still open upstream.

## Current branch roles

- `main` contains the actively developed CoDriver version and remains the head branch of the open CoDriver skin pull request.
- `upstream-main` starts from the current `zhukunpenglinyutong/jetbrains-cc-gui` `main` release state and is kept as the stable upstream reference.

## Planned branch rename

Do **not** perform these renames until the CoDriver skin pull request has been merged upstream.

After the CoDriver skin pull request is merged, rename the branches in this exact order:

1. Rename `main` to `dev`.
2. Rename `upstream-main` to `main`.

The order is intentional: the existing `main` name must be released before `upstream-main` can be renamed to `main`.

After that transition:

- `main` will represent the current released upstream baseline.
- `dev` will represent the current development version plus any fork-specific work that has not yet been merged upstream.
