# craftor/homebrew-task-manager

Homebrew tap for [craftor/task-manager](https://github.com/craftor/task-manager).

The macOS `.dmg` in the upstream repo's GitHub Releases is ad-hoc signed
(no paid Apple Developer Program), so opening it directly triggers a
Gatekeeper warning. Homebrew installs casks by stripping the quarantine
attribute, sidestepping the warning.

## Install

```bash
brew tap craftor/task-manager
brew install --cask task-manager
```

## Upgrade

```bash
brew update && brew upgrade --cask task-manager
```

## How this tap is updated

See `packaging/homebrew/README.md` in the upstream repo. The maintainer
runs `scripts/update_cask_sha.sh` after each release, which patches the
cask's `version` and `sha256` from the GitHub Releases API, then copies
`Casks/task-manager.rb` here.
