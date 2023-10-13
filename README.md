List and checkout git previously used branches.

## Installation

Put the `git-branch-history` executable to your path.

For example you can use the following command.
```sh
echo 'export PATH=$PATH:'$PWD >> ~/.profile
```

Maybe you'll need to relogin or open a new shell - depends on how do you
configure the $PATH.

Then you can use `git branch-history` command to execute the command.

### Save the branch on every branch change

#### set alias

You might want to set an alias to save some typing

```sh
git config --global alias.bh branch-history
```

## Usage

Checkout to previous branch

```sh
git branch-history previous
# in short
git branch-history p
```

List the history:

```sh
git branch-history list
# in short
git branch-history ls
```

Checkout branch used before the previous branch:

```sh
git branch-history previous-n 2
# in short
git branch-history n 2
```
