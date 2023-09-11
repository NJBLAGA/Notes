# Tmux Commands

## **Basics**

**`Control + Space`** Prefix

**`Prefix + Shift + r`** Plugins — Reload Config File

**`Prefix + Shift + i`** Install Plugins

**`Prefix + c`** Create Window

**`Prefix + s`** List all Sessions

`Shift + Alt + h` Switch Previous Window

`Shift + Alt + l` Switch Next Window

**`Prefix + w`** Toggle window tree

**`Prefix + f`** Toggle window find

`**Type exit** **| Prefix + &`\*\* Kill `Tmux`

`Shift  + Alt + v` Paste from `System Clipboard`

## Copy Mode **Basic**

`**Prefix + [**` vi Mode

`**v**` Select Mode

`y` Yank

`Control + v` Toggle Line/Rectangle Mode

`Prefix + =` Display content in Buffer

`**Prefix + ]**` Paste

## **Panes Basic**

**`Prefix + v`** Vertical Pane

**`Prefix + h`** Horizontal Pane

**`Prefix + x`** Close Pane

`Control + h` Switch Pane Right

`Control + l` Switch Pane Left

`Control + j` Switch Pane Up

`Control + k` Switch Pane Down

**`Prefix + Control + Arrow Key`** Resize Panes

## **Session Management**

`tmux` Create new session

`tmux new -s [session-name]` Create new named session

**`tmux ls`** View Sessions

**`Prefix + d`** Detach Session

**`tmux attach | a`** Open Last Session

**`Tmux a -t<number>`** Open Session n
