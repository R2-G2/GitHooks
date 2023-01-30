<!-- Copyright (c) 2022 Ralf Grawunder -->

# GitHooks: my Git hooks

## Setup

Create the *hooks templatedir*.

```shell
mkdir -p ~/.gittemplates/hooks
```

Announce the directory to **Git**.

```shell
editor ~/.gitconfig
```

```gitconfig
[init]
	templatedir = ~/.gittemplates
```

### post-commit

Install **sl** (Steam Locomotive) and create a symlink.

```shell
ln -s "$(readlink -m ./post-commit.sh)" ~/.gittemplates/hooks/post-commit
```

## Problems?

Fork! Fork it! Fork you! Fork me, right?
