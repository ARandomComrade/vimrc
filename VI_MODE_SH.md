# Vi Mode Configurations for Common Shells
Just some ways here to set vi mode features on every shell and command line I've run into...
## GNU Readline
Append to ```.inputrc```. This sets it for things that use Readline to handle interactive command line inputs like Python, Nodejs, MySql, GDB and yes, Bash. 
```sh
set editing-mode vi
```
If you're on windows and using cmd.exe, this is how you set it with Clink, same file too.
Also set ```$EDITOR``` if you want Readline to be able to edit your terminal commands in Vim.
```sh
# Bash only
export EDITOR=$(which vim)
# POSIX COMPATIBLE!
export EDITOR=`which vim`
```
```cmd
rem Windows command line
set EDITOR="vim"
```
```ps1
# PowerShell
$env:EDITOR="vim"
```

## Bash
Append to your ```.bashrc``` or you can run it in a session.
```sh
set -o vi
```

## Ksh88/Ksh93
Append to ```.kshrc``` or ```.profile``` or you can run it in a session. (Same way it's done in bash).
```sh
set -o vi
```

## Csh/Tcsh (Mainly Tcsh though...)
Append to ```.cshrc``` or ```.tcshrc```. You can also run it in a session. (Same way it's done in Zsh).
```sh
bindkey -v
```

## Zsh
Append to ```.zshrc```. FYI, Zsh asks you if you want to set this during the **zsh-newuser-install** wizard. This is here for completeness plus in case you missed it. You can also run this in a session.
```sh
bindkey -v
```

## Fish
Add this to ```~/.config/fish/config.fish```. You can also run this in a session.
```sh
set -g fish_key_bindings fish_vi_key_bindings
```

## PowerShell
Add this to your ```$PROFILE```. You can also run it in a session.
```ps1
Set-PSReadLineOption -EditMode Vi
```