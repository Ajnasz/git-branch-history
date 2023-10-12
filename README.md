Record branch git history so you can switch back to previous used branches more
easily.

## Installation

Put the `git-branch-history` executable to your path.

For example you can use the following command.
```sh
echo 'export PATH=$PATH:'$PWD >> ~/.profile
```

Maybe you'll need to relogin or open a new shell - depends on how do you
configure the $PATH.

Then you can use `git branch-history` command to execute the command.

Run `git branch-history save` command whenever want to record the current
branch.

### Save the branch on every branch change

You can run the command and save the history automatically on every branch
change if you add the `git branch-history save` action as a git `post-checkout`
hook.

Check if you already have it configured:
```sh
git config --global --get core.hookspath
```

#### core.hookspath not configured

Run the following command:

```sh
mkdir ~/.git-hooks
cp $PWD/git-hooks/post-checkout $HOME/.git-hooks/
git config --global core.hookspath $HOME/git-hooks
```

#### core.hookspath configured

If it set for you, open the `post-checkout` file there and add the save content
of the post-checkout file with what you can see in
[git-hooks/post-checkout](./git-hooks/post-checkout).

!important that here you can use the `-g` flag which indicates that no need to
check if the command called from a git repository - so it will run a bit
faster.
