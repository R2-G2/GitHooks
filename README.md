<!-- Copyright (c) 2022-2023 Ralf Grawunder -->

# GitHooks: my default Git hooks

## Setup

### Universal

Create the *hooks templatedir*.

```shell
mkdir -p /CUSTOM/PATH/hooks
```

Announce the *templatedir* to **Git**.

```shell
editor /PATH/TO/.gitconfig
```

```gitconfig
[init]
	templatedir = /CUSTOM/PATH
```

### Personal

```shell
mkdir -p ~/.gittemplates/hooks
vim ~/.gitconfig
```

```gitconfig
[init]
	templatedir = ~/.gittemplates
```

## Usage

### post-commit

First install **sl** (Steam Locomotive) and then create a symlink.

After committing, a steam locomotive will cross the terminal, trying to prevent you from pushing to early. **Spoiler:**
This won't always help!

#### Universal

```shell
ln -s "$(readlink -m ./post-commit.sh)" /CUSTOM/PATH/hooks/post-commit
```

#### Personal

```shell
ln -s "$(readlink -m ./post-commit.sh)" ~/.gittemplates/hooks/post-commit
```

## Problems?

Fork! Fork it! Fork you! Fork me, right?
