# .Dot files


### Symlinks and home directory

**Bash**

On different systems you may have a `.bash_profile`, `.bashrc` and `.profile` files. We need to direct configuration to our dotfiles directory. Edit your files to include the following.

**.bash_profile**

```
if [ -f ~/.bashrc ];
then
    source ~/.bashrc
fi
```

**.bashrc**

```
. ~/bin/dotfiles/bash/env
. ~/bin/dotfiles/bash/config
. ~/bin/dotfiles/bash/aliases
```


**Git**

Symlink the following files/directories to the dotfiles directory.

```
.git_template -> bin/dotfiles/git/.git_template
.gitconfig -> /Users/yourusername/bin/dotfiles/git/.gitconfig
.gitconfig_local
.gitignore -> /Users/yourusername/bin/dotfiles/git/.gitignore
git-completion.bash -> /Users/yourusername/bin/dotfiles/git/git-completion.bash
git-flow-completion.bash -> /Users/yourusername/bin/dotfiles/git/git-flow-completion.bash
```
