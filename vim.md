---
title: Vim
category: Vim
layout: 2017/sheet
tags: [Featured]
updated: 2018-09-11
weight: -10
intro: |
 [Vim](http://www.vim.org/) is a very efficient text editor. This reference was made for Vim 8.0.   
 For shortcut notation, see `:help key-notation`.
 
 This cheatsheet assumes you are using these rc files and plugins [https://github.com/karamfil/saphe/tree/master/vim]
 
 A lot of vim commands/motions can use counters example `10w`
---


Getting started
---------------
{: .-three-column}


### Modes
{: .-prime}

#### Modes

| Shortcut     | Description                            |
| ---          | ---                                    |
| `normal`    | For navigation and manipulation of text. This is the mode that vim will usually start in, which you can usually get back to with ESC and shuold be spending most time in this mode. <br />`:help normal-mode` |
| `insert`    | For inserting new text. <br />`:help insert-mode` |
| `visual`    | For navigation and manipulation of text selections, this mode allows you to perform most normal commands and a few extra commands on selected text. <br />`:help visual-mode` |
| `block visual` | Similar to visual mode but working on a block instead <br />`:help visual-block` |
| `select`    | Similar to visual, but with a more MS Windows-like behavior. <br />`:help select-mode` |
| `command`   | For entering editor commands - like the help commands for example. <br />`:help command-line-mode` |
| `ex-mode`   | Similar to the command-line mode but optimized for batch processing. <br />`:help ex-mode` |
{: .-shortcuts}

### Writing and Quitting
{: .-prime}


#### Writing

`!` Means force a command

| Shortcut       | Description                            |
| ---            | ---                                    |
| `:w`           | Write                                  |
| `:wq` _/_ `:x` | Write and Quit file                    |
| `:wa`          | Write all bufers Quit file             |
| `:[range]w[!]` | Write [range] [force]                  |
| `:w {file}`    | Write to a new file                    |
| `:up`          | Update - write to file if modified     |
{: .-shortcuts}

#### Quitting

| Shortcut       | Description                            |
| ---            | ---                                    |
| `:q`           | Quit file                              |
| `:q!`          | Quit file, abandon changes (force)     |
| `:qa`          | Quit all files                         |
| `:qa!`         | Quit all files, abandon changes        |
| `:cq[uit]`     | Works like `:qa`, but throws an error. Great for aborting Git commands. |
{: .-shortcuts}


#### Misc

| Shortcut       | Description                            |
| ---            | ---                                    |
| `ZZ`           | Write and quit (same as :x | :wq)      |
| `ZQ`           | Froce Quit (as :q!)                    |
| ---            | ---                                    |
| `:st[!]`       | Stop                                   |
| `<C-Z>`        | Same as :stop                          |
{: .-shortcuts}

#### History

| Shortcut | Description                         |
| ---      | ---                                 |
| `u`      | Undo changes                        |
| `U`      | Restore last changed line           |
| `<C-R>`  | Redo changes                        |
{: .-shortcuts}



### Exiting insert mode

| Shortcut          | Description |
| ---               | ---         |
| `Esc` _/_ `<C-[>` | Exit insert mode |
| `<C-C>`           | Exit insert mode, and abort current command |
{: .-shortcuts}

### Counters

| Shortcut | Description      |
| ---      | ---              |
| `<C-A>`  | add N to the number at or after the cursor |
| `<C-X>`  | subtract N to the number at or after the cursor |
{: .-shortcuts}

### Text alignment

    :center [width]
    :right [width]
    :left
{: .-shortcuts}


### Motions

#### Repeat

TBD Link to repeatable motions config

| Shortcut            | Description          |
| ---                 | ---                  |
| `;`                 | Forwards last motion   |
| `,`                 | Backwards last motion   |
{: .-shortcuts}

#### Base

| Shortcut            | Description          |
| ---                 | ---                  |
| `h` `j` `k` `l`     | ← ↑ ↓ →             |
| ---                 | ---                  |
| `0`          | Start of line               |
| `^`          | First non-blank character   |
| `$`          | End of line                 |
| `10|`        | to column 10 |
{: .-shortcuts}

#### Words

Big WORDS are whitespace delmited

| Shortcut     | Description               |
| ---          | ---                       |
| `w` | Next word        |
| `W` | Next WORD        |
| `b` | Back word        |
| `B` | Back WORD        |
| `e` | End of word |
| `E` | End of WORD |
| `ge` | end of last word |
| `gE` | end of last WORD |
{: .-shortcuts}


#### Character

| `fc`  | find character `c`  |
| `Fc`  | find character `c` backwards |
| `tc`  | Till character `c` |
| `Tc`  | Till character `c` backwards |
{: .-shortcuts}

#### Document

| Shortcut | Description    |
| ---      | ---            |
| `gg`     | First line     |
| `G`      | Last line      |
| `:10`     | Go to line `10` |
| `10G`     | Go to line `10` |
{: .-shortcuts}

### Editing

| Shortcut | Description                         |
| ---      | ---                                 |
| `.`      | Repeat last edit command            |
| ---      | ---                                 |
| `a`      | Append after caret                  |
| `A`      | Append at the end of line           |
| `i`      | Insert before caret                 |
| `I`      | Insert before first non-blanc character of line |
| `gI`      | Insert at the begining of line                 |
| `gi`      | Insert text in the same position as where Insert mode was stopped last time in the current buffer |
| ---      | ---                                 |
| `o`      | Open next line                      |
| `O`      | Open previous line                  |
| ---      | ---                                 |
| `s`      | Substitude character                |
| `S`      | Substitude line                     |
| `C`      | Change until end of line            |
| ---      | ---                                 |
| `x`      | Delete character under caret    |
| `X`      | Delete character before caret    |
| `D`      | Delete to the end of line                         |
| ---      | ---                                 |
| `J`      | Join Lines               |
| `gJ`      | Join Lines without whitespace              |
| ---      | ---                                 |
| `<C-A>`      | add N to the number at or after the cursor             |
| `<C-X>`      | subtract N to the number at or after the cursor              |
| ---      | ---                                 |
| `r`      | Replace one character               |
| `R`      | Enter Replace mode                  |
{: .-shortcuts}


### Navigation
{: .-prime}

| Shortcut            | Description                |
| ---                 | ---                        |
| `(` | Move sentence backward |
| `)` | Move sentence forward |
| `{` | Move pargraph backward |
| `}` | Move pargraph forward 
| ---                 | ---                        |
| `%`                | matching brace, bracket, etc      |
| ---                 | ---                        |
| `[m`                | back to method start      |
| `[M`                | back to method end        |
| `]m`                | forward to method start      |
| `]M`                | forward to method end        |
| `[*` _/_ `[/` | back to start of comment `/*` |
| `]*` _/_ `]/` | forward to end of comment `*/` |
| ---                 | ---                        |
| `[(` | back to unclosed `(` |
| `[{` | back to unclosed `{` |
| `[#` | back to unclosed `#if` or `#else` |
| `])` | forward to unclosed `)` |
| `]}` | forward to unclosed `}` |
| `]#` | forward to unclosed `#if` or `#else` |
{: .-shortcuts}


#### Window

| Shortcut | Description              |
| ---      | ---                      |
| `H`      | Move to top (High) of screen    |
| `M`      | Move to Middle of screen |
| `L`      | Move to bottom (Low) of screen |
| --- | --- |
| `zt`     | Move line in the top         |
| `zz`     | Move line in the middle         |
| `zb`     | Move line in the bottom         |
{: .-shortcuts}

#### Scrolling

| Shortcut            | Description       |
| ---                 | ---               |
| `<C-B>` | Move full page Backwards |
| `<C-F>` | Move full page Forwards |
| ---                 | ---               |
| `<C-U>` | Move half page up |
| `<C-D>` | Move half Page down |
| --- | --- |
| `<C-E>` | Page line up (extra line) |
| `<C-Y>` | Page line down (yester line) |
{: .-shortcuts}

### Jumping

| Shortcut | Description                  |
| ---      | ---                          |
| `<C-O>`  | Go back to previous location |
| `<C-I>`  | Go forward                   |
{: .-shortcuts}




Operators
---------
{: .-three-column}

### Usage
{: .-prime}

Operators let you operate in a range of text (defined by *motion*). These are performed in normal mode.
{: .-setup}

| `d`      | `w`    |
| Operator | Motion |
{: .-css-breakdown}

### Operators

| Shortcut | Description                     |
| ---      | ---                             |
| `d{motion}`      | Delete                          |
| `y{motion}`      | Yank _(copy)_                   |
| `c{motion}`      | Change _(delete then insert)_   |
| ---      | ---                             |
| `>{motion}`      | Indent right                    |
| `<{motion}`      | Indent left                     |
| `={motion}`      | Reindent                     |
| ---      | ---                             |
| `g~{motion}`     | Swap case                       |
| `gU{motion}`     | Uppercase                       |
| `gu{motion}`     | Lowercase                       |
{: .-shortcuts}

### Shortcuts

| Shortcut | Description                     |
| ---      | ---                             |
| `dd`      | Delete line                         |
| `yy` _/_ `Y` | Yank line                   |
| `cc`      | Change line   |
| ---      | ---                             |
| `>>`      | Indent line right                    |
| `<<`      | Indent line left                     |
| `==`      | Reindent line                     |
| ---      | ---                             |
| `g~~`     | Swap case line                       |
| `gUU`     | Uppercase line                       |
| `guu`     | Lowercase line                       |
{: .-shortcuts}

| Shortcut | Description                     |
| ---      | ---                             |
| `>>`      | Indent line right                    |
| `<<`      | Indent line left                     |
| ---      | ---                             |
| `g~~`     | Swap case line                       |
| `gUU`     | Uppercase line                       |
| `guu`     | Lowercase line                       |
{: .-shortcuts}

### Surround (Plugin)

Surround plugin works with lots of charracters `"` `'` <code>`</code> `(` `)` `[` `]` `{` `}` `<` `>` ...

| Shortcut      | Description                     |
| ---           | ---                             |
| `ys{motion}"` | Yank surround {motion} or {text object} with `"..."`
| `ys{motion}{` | Yank surround {motion} or {text object} with `{...}` with spacing
| `ys{motion}}` | Yank surround {motion} or {text object} with `{...}` without spacing
| ---           | ---                             |
| `cs"'`        | Change surrounding `"` with `'` |
| `ds"`         | Delete surrounding `"` |

{: .-shortcuts}



Text objects
------------
{: .-three-column}

### Usage
{: .-prime}

Text objects let you operate (with an *operator*) in or around text blocks (*objects*).
{: .-setup}

| `v`      | `i`                  | `p`         |
| Operator | [i]nside or [a]round | Text object |
{: .-css-breakdown}

### Text objects

| Shortcut               | Description           |
| ---                    | ---                   |
| `p`                    | Paragraph             |
| `w`                    | Word                  |
| `s`                    | Sentence              |
| ---                    | ---                   |
| `[` `(` `{` `<`        | A [], (), or {} block |
| `'` `"` <code>`</code> | A quoted string       |
| ---                    | ---                   |
| `b`                    | A block [(            |
| `B`                    | A block in [{         |
| `t`                    | A XML tag block       |
| `i`                    | intented block        |
{: .-shortcuts}

### Examples

| Shortcut    | Description                        |
| ---         | ---                                |
| `vii`       | Select paragraph                   |
| ---         | ---                                |
| `yip`       | Yank inner paragraph               |
| `yap`       | Yank paragraph (including newline) |
| ---         | ---                                |
| `diw`       | Delete inner word             |
| `ciw`       | Change inner word             |
| `ci{`       | Change inner { ... }          |
{: .-shortcuts}


TODO
----


TODO
----


TODO
----


TODO
----

Commentary Plugin

Easy Align Plugin

Easy Motion Plugin

Nerd Tree Plugin


TODO
----


### Special keys in Insert mode

i_CTRL-V      CTRL-V {char}..   insert character literally, or enter decimal
                                     byte value
i_<NL>        <NL> or <CR> or CTRL-M or CTRL-J
                                  begin new line
i_CTRL-E      CTRL-E            insert the character from below the cursor
i_CTRL-Y      CTRL-Y            insert the character from above the cursor

i_CTRL-A      CTRL-A            insert previously inserted text
i_CTRL-@      CTRL-@            insert previously inserted text and stop
                                     Insert mode
i_CTRL-R      CTRL-R {0-9a-z%#:.-="}  insert the contents of a register

i_CTRL-N      CTRL-N            insert next match of identifier before the
                                     cursor
i_CTRL-P      CTRL-P            insert previous match of identifier before
                                     the cursor
i_CTRL-X      CTRL-X ...        complete the word before the cursor in
                                     various ways

i_<BS>        <BS> or CTRL-H    delete the character before the cursor
i_<Del>       <Del>             delete the character under the cursor
i_CTRL-W      CTRL-W            delete word before the cursor
i_CTRL-U      CTRL-U            delete all entered characters in the current
                                     line
i_CTRL-T      CTRL-T            insert one shiftwidth of indent in front of
                                       the current line
i_CTRL-D      CTRL-D            delete one shiftwidth of indent in front of
                                     the current line
i_0_CTRL-D    0 CTRL-D          delete all indent in the current line
i_^_CTRL-D    ^ CTRL-D          delete all indent in the current line,
                                     restore indent in next line


TODO
----


### Repeating commands

.        N  .         repeat last change (with count replaced with N)
q           q{a-z}    record typed characters into register {a-z}
q           q{A-Z}    record typed characters, appended to register {a-z}
q           q         stop recording
@        N  @{a-z}    execute the contents of register {a-z} (N times)
@@       N  @@           repeat previous @{a-z} (N times)
:@       :@{a-z}      execute the contents of register {a-z} as an Ex
                           command
:@@      :@@          repeat previous :@{a-z}
:g       :[range]g[lobal]/{pattern}/[cmd]
                        execute Ex command [cmd] (default: ":p") on the lines
                           within [range] where {pattern} matches
:g       :[range]g[lobal]!/{pattern}/[cmd]
                        execute Ex command [cmd] (default: ":p") on the lines
                           within [range] where {pattern} does NOT match
:so      :so[urce] {file}
                        read Ex commands from {file}
:so      :so[urce]! {file}
                        read Vim commands from {file}
:sl      :sl[eep] [sec]
                        don't do anything for [sec] seconds
gs       N  gs        goto Sleep for N seconds




### Clipboard and Marks

| `p`      | Paste               |
| `P`      | Paste before        |
| `]p` | like p, but adjust indent to current line |
| `[p` | like P, but adjust indent to current line |
| `gp` | like p, but leave caret after the new text |
| `gP` | like P, but leave caret after the new text |
| registers ||

### Marks and motions

m        m{a-zA-Z}    mark current position with mark {a-zA-Z}
`a       `{a-z}       go to mark {a-z} within current file
`A       `{A-Z}       go to mark {A-Z} in any file
`0       `{0-9}       go to the position where Vim was previously exited
``       ``           go to the position before the last jump
`quote   `"           go to the position when last editing this file
`[       `[           go to the start of the previously operated or put text
`]       `]           go to the end of the previously operated or put text
`<       `<           go to the start of the (previous) Visual area
`>       `>           go to the end of the (previous) Visual area
`.       `.           go to the position of the last change in this file
'        '{a-zA-Z0-9[]'"<>.}
                        same as `, but on the first non-blank in the line
:marks  :marks        print the active marks
CTRL-O  N  CTRL-O     go to Nth older position in jump list
CTRL-I  N  CTRL-I     go to Nth newer position in jump list
:ju     :ju[mps]      print the jump list



### Marks

| Shortcut        | Description                                        |
| ---             | ---                                                |
| <code>`^</code> | Last position of cursor in insert mode             |
| <code>`.</code> | Last change                                        |
| <code>``</code> | Last jump                                          |
| ---             | ---                                                |
| `ma`            | Mark this cursor position as `a`                   |
| <code>`a</code> | Jump to the cursor position `a`                    |
| `'a`            | Jump to the beginning of the line with position `a`|
{: .-shortcuts}


### Visual mode

visual-index  list of Visual mode commands.

v        v            start highlighting characters  }  move cursor and use
V        V            start highlighting linewise    }  operator to affect
CTRL-V   CTRL-V       start highlighting blockwise   }  highlighted text
v_o      o            exchange cursor position with start of highlighting
gv       gv           start highlighting on previous visual area
v_v      v            highlight characters or stop highlighting
v_V      V            highlight linewise or stop highlighting
v_CTRL-V CTRL-V       highlight blockwise or stop highlighting


### Visual mode

| Shortcut | Description             |
| ---      | ---                     |
| `v`      | Enter visual mode       |
| `V`      | Enter visual line mode  |
| `<C-V>`  | Enter visual block mode |
{: .-shortcuts}


Misc
----

### Folds

Needs a foldmethod to be set ex: `:set foldmethod=syntax`

'foldmethod'
    set foldmethod=manual   manual folding
    set foldmethod=indent   folding by indent
    set foldmethod=expr     folding by 'foldexpr'
    set foldmethod=syntax   folding by syntax regions
    set foldmethod=marker   folding by 'foldmarker'

zf            zf{motion}              operator: Define a fold manually
:fold         :{range}fold            define a fold for {range} lines
zd            zd                      delete one fold under the cursor
zD            zD                      delete all folds under the cursor

zo            zo                      open one fold under the cursor
zO            zO                      open all folds under the cursor
zc            zc                      close one fold under the cursor
zC            zC                      close all folds under the cursor

zm            zm                      fold more: decrease 'foldlevel'
zM            zM                      close all folds: make 'foldlevel' zero
zr            zr                      reduce folding: increase 'foldlevel'
zR            zR                      open all folds: make 'foldlevel' max.

zn            zn                      fold none: reset 'foldenable'
zN            zN                      fold normal set 'foldenable'
zi            zi                      invert 'foldenable'

| Shortcut      | Description                  |
| ---           | ---                          |
| `zo` _/_ `zO` | Open                         |
| `zc` _/_ `zC` | Close                        |
| `za` _/_ `zA` | Toggle                       |
| ---           | ---                          |
| `zv`          | Open folds for this line     |
| ---           | ---                          |
| `zM`          | Close all                    |
| `zR`          | Open all                     |
| ---           | ---                          |
| `zm`          | Fold more _(foldlevel += 1)_ |
| `zr`          | Fold less _(foldlevel -= 1)_ |
| ---           | ---                          |
| `zx`          | Update folds                 |
{: .-shortcuts}

Uppercase ones are recursive (eg, `zO` is open recursively).






### Windows

| `z{height}<Cr>` | Resize pane to `{height}` lines tall |

### Tags

| Shortcut              | Description                                     |
| ---                   | ---                                             |
| `:tag Classname`      | Jump to first definition of Classname           |
| ---                   | ---                                             |
| `<C-]>`               | Jump to definition                              |
| `g]`                  | See all definitions                             |
| `<C-T>`               | Go back to last tag                             |
| `<C-O> <C-I>`         | Back/forward                                    |
| ---                   | ---                                             |
| `:tselect Classname`  | Find definitions of Classname                   |
| `:tjump Classname`    | Find definitions of Classname (auto-select 1st) |
{: .-shortcuts}


### Command line

| Shortcut     | Description                               |
| ---          | ---                                       |
| `<C-R><C-W>` | Insert current word into the command line |
| `<C-R>"`     | Paste from " register                     |
| `<C-X><C-F>` | Auto-completion of path in insert mode    |
{: .-shortcuts}


See `:help formatting`

### Calculator

| Shortcut      | Description                               |
| ---           | ---                                       |
| `<C-R>=128/2` | Shows the result of the division : '64'   |

Do this in insert mode.


Also see
--------

- [Vim cheatsheet](https://vim.rtorr.com/) _(vim.rotrr.com)_
- [Vim documentation](http://vimdoc.sourceforge.net/htmldoc/) _(vimdoc.sourceforge.net)_
- [Interactive Vim tutorial](http://openvim.com/) _(openvim.com)_
