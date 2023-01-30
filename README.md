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
editor /PATH/TO/YOUR/.gitconfig
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

### Use post-commit

First install **sl** (Steam Locomotive).

### Universal

Now you could create a copy of the script.

```shell
cp ./post-commit.sh /CUSTOM/PATH/hooks/post-commit
```

The best way may be to create a symlink.

```shell
ln -s "$(readlink -m ./post-commit.sh)" /CUSTOM/PATH/hooks/post-commit
```

### Personal

```shell
ln -s "$(readlink -m ./post-commit.sh)" ~/.gittemplates/hooks/post-commit
```

## Problems?

Fork! Fork it! Fork you! Fork me, right?
