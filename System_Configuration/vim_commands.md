# **Vim/NeoVim Commands**

## **Basics**

`!` - Force Command

`Space` Leader Key

`Space **+ t + h`\*\* Change Theme

## **Quit**

`:q` Quit file

`:q!` Quit without saving changes

`:wq` Write file then quit

## **Show Info**

`Control + g` Show file name and current location

`g + Control + g` More detailed information

## **Help**

`:h` Help Window

`:h [command]` Help window on desired `[command]`

## **Navigation**

`h` Move Left

`l` Move Right

`j` Move Down

`k` Move Up

`w` Jump forward one word

`shift + w` Jump forward one word (ignore white spaces)

`b` Jump backward one word

`Shift + b` Jump backward one word (ignore white spaces)

`Shift + [ or ]`Move by paragraph

`Control + d` Move down

`Control + u` Move down

`Shift + 0`  Jump to start of line

`Shift + ^` Jump to first character in the line

`Shift + $` Jump to end of line

`g + g` Move to start of the file

`G` Move to bottom of the file

`[number] + g + g` move to line `number`

`:[number]` Cursor on line `[number]`

`Control + f` To move down one page

`Control + b` To move back up one page

## **Panes**

`:vsp` New Vertical Split

`:sp` New Spilt

`Control +h` Move Left

`Control +l` Move Right

`Control + j` Move Down

``Control + k` Move Up

## **Normal Mode**

`Control + s` Save

`Space + /` Toggle comment

## **Insert Mode**

`i` Insert mode (cursor before char)

`a` Append mode (cursor after char)

`Control + b` Beginning of Line

`Control + e` End of Line

`Control + h` Move Left

`Control + l` Move Right

`Control + j` Move Down

`Control + k` Move Up

## Visual **Mode**

`Modes`

`v` Toggle Visual `Character` mode

`Shift + v` Toggle Visual `Linewise` mode

`Control + v` Toggle Visual `Blockwise`Block

`h` Move Left

`l` Move Right

`j` Move Down

`k` Move Up

`o` Expands start of line

`Shift + o` Expands end of line

`ap` Highlight paragraph

`>` Tabs text to right

`gv + <` Tabs text to left

## **Delete**

`x` Delete next character

`Shift + x` Delete prev character

`d + w` Delete word

`d + e` Delete to the end of the current word

`d + d` Delete entire line

`d + $` Delete till end of line

`d  + ^` Delete till start of line

`d + [h,j,k,l]` Delete motions

## **Paste/Put**

`p` Paste

`Shit + p` Paste above line

## Copy/Yank

`y` Yank

`y + y` Yank Line

`y + w` Yank word

`Control + c` Copy All

## Move Lines

`d + d + j + P` Move Line Up

`d + d + p` Move Line Down

## **Undo & Redo**

`u` Undo last command

`Shift + u` Undo line only

`Control + r` Redo last command

## Text Objects

`[operator] + a + [object]` Change a word

`[operator] + i + [object]` Change inner word

`s` Change sentence

`p` Change paragraph

`b` Change `()`

`[` Change Arrays

`B` Change Object

`<>` HTML Tags

`cit` Change Inner Text

`cat` Change tag

`"Hello World"` Change Double Quotes

## Insert

`Shift + i` Insert mode at first character

`a` Append text to right of cursor

`Shift a` Append text to end of line

`o` New line below cursor

`Shift + o` New line above cursor

`[count] + o + #  + esc` Create 5 new lines with `#`

## **Registers**

`:reg` Displays all registers

`"[register]" + [comannd]` Select desired register

`"[register [a-z]] + [command]` Store in`register`

## Change & **Replace**

`Shift + r` Replace mode

`r` Replace `1` character

`c` Change Command

`c + w [word replacement]` Replace word

`c + c` Change whole line

`Shift + tilda` Capitalise character

`g + Shift U + [motion]` Upper case characters

`g + u + [motion]` Lower case characters

## Join

`Shift + j` Join Command

`g + Shift j` Join without spaces

## Search, Find & Replace

`f` Find Command

`f + y` Finds first `y` character

`f + Shift + y` Finds first `Y` character

`;` Cursor moves to next character

`,` Cursor moves to prev character

`t + [character]` Move cursor to letter before `character`

`Shift t + [character]` Move cursor to letter after `character`

`/ [phrase]` Search Command

`n` Tab

`Shift + n` Tab reverse

`:set hls` Set `hls` true

`:s/old/new` Sub old phrase for new phrase

`:s/old/new/[flags]`

`g` Change all phrases on line

`:[range]s/old/new/[flag]` line number `1,5`

`1` First line

`$` Last line

`.` Current line

`%` All lines

`:/[pattern1]/,/[pattern2]/s/[old/new/[flag]` Change phrases between patterns

`? [phrase]` Reverse search

## Buffers

`:ls` Display all buffers

`:b[buffer-name]` Open buffers

`Space + b` New Buffer

`Space + x` Close Buffer

`Tab` Cycle Next Buffers

`Shift + Tab` Cycle Previous Buffers

## Terminal

`Space + v` New Vertical Terminal

`Space + h` New Vertical Terminal

`Alt + i` Toggle Floating Terminal

`Alt + v` Toggle Vertical Terminal

`Alt + i` Toggle Floating Terminal

`Space + h` Toggle Vertical Terminal

## Macros

`q` Macro Command

`q "a` Record macro in register `a`

`q` End Recording

`@ [register]` Execute certain register macro

`@@` Run last Macro

## Which Key

`Space + w + k` Which Key Lookup/Key Maps

# **Plugins**

## M**arkdown Preview**

`Space + m + p`

## Live Server

`npm i -g liver-server` Install

`live-server [html file]` Launch file

`live-server [directory]` Launch directory
