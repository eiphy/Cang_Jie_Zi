<!-- ### <a name="table"></a>Table -->

Migrate to neo vim. Use Neo vim for vscode too.

### Table

Part 1 Practical Usage
- [Navigation](#Navigation)
- [File Operation & Window Management](#File-Operation-&-Window-Management)
- [Regular Experssion](#Regular-Expression)
- [Command](#Vim-Command)

Part 2 VIM
- [General](#General)
- [Register](#Register)
- [Options](#Options)

### Navigation

Moving:

Ctrl+f (Next page) and Ctr+b (Last page)

50+%

CTRL + ]: go to the tag.

:num / numG

search and substitution.

g/gc

\c ignore case

### File Operation & Window Management

File Operation:

Window Management:

':q' close window;

':qa!' quit vim.

:w FILENAME

:r FILENAME / :r !command (Retrival content from a file)

<C-G> check file status.

### Regular Expression

/^$ 

(This is not supported by the vscode vim extention.
It seems that the extension does not support many regular expression)

/^I^I

Have difficulty using in both vim and vscode extention.

### Vim Command

:set list		Show  \t and end of the line (:set nolist)

:set fileencoding	Show encoding

:e ++enc=utf-8		Set encoding

<br></br>
<br></br>

:n,md
noremap d "\_d		d will not save content to clipboard, Use V+x instead.

### General

Commands in vim are usually formed by: operator [number] motion.

Operator: c, d.

Motions: w, e, $.

External command: !

### Register

### Options
:set ic / noic Ignore case
:set hlsearch Highlight search
:set is Increment search



[Table](#Table)
