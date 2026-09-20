# Vim Editor Commands

## 1. What is Vim?

Vim is a terminal-based text editor used to create, edit, and modify files.

Start Vim:

```bash
vim filename
```

Example:

```bash
vim notes.txt
```

---

# 2. Vim Modes

Vim mainly has these modes:

| Mode         | Purpose                       | Enter         |
| ------------ | ----------------------------- | ------------- |
| Normal Mode  | Navigate and perform commands | `Esc`         |
| Insert Mode  | Type/write text               | `i`, `a`, `o` |
| Visual Mode  | Select text                   | `v`           |
| Command Mode | Save, quit, search, etc.      | `:`           |

When Vim opens, you are normally in **Normal Mode**.

To return to Normal Mode:

```text
Esc
```

---

# 3. Open a File

```bash
vim filename
```

Example:

```bash
vim notes.txt
```

Open a specific file:

```bash
vim /home/siddhant/notes.txt
```

Open multiple files:

```bash
vim file1.txt file2.txt
```

---

# 4. Insert Mode

## `i`

Starts typing before the current character.

```text
i
```

---

## `I`

Starts typing at the beginning of the current line.

```text
I
```

---

## `a`

Starts typing after the current character.

```text
a
```

---

## `A`

Starts typing at the end of the current line.

```text
A
```

---

## `o`

Creates a new line below the current line and enters Insert Mode.

```text
o
```

---

## `O`

Creates a new line above the current line and enters Insert Mode.

```text
O
```

---

## `Esc`

Returns to Normal Mode.

```text
Esc
```

---

# 5. Moving Around

## `h`

Move left.

```text
h
```

---

## `l`

Move right.

```text
l
```

---

## `j`

Move down.

```text
j
```

---

## `k`

Move up.

```text
k
```

Remember:

```text
      k
      ↑
h ←       → l
      ↓
      j
```

---

## Arrow Keys

You can also use:

```text
↑
↓
←
→
```

---

# 6. Moving by Words

## `w`

Move to the beginning of the next word.

```text
w
```

---

## `b`

Move to the beginning of the previous word.

```text
b
```

---

## `e`

Move to the end of the current/next word.

```text
e
```

---

## `0`

Move to the beginning of the line.

```text
0
```

---

## `^`

Move to the first non-space character of the line.

```text
^
```

---

## `$`

Move to the end of the line.

```text
$
```

---

# 7. Moving in the File

## `gg`

Go to the first line of the file.

```text
gg
```

---

## `G`

Go to the last line.

```text
G
```

---

## `numberG`

Go to a specific line.

```text
10G
```

Goes to line 10.

Example:

```text
25G
```

Goes to line 25.

---

## `:number`

Go to a specific line.

```text
:10
```

Example:

```text
:25
```

---

## `Ctrl + f`

Move one screen forward.

```text
Ctrl + f
```

---

## `Ctrl + b`

Move one screen backward.

```text
Ctrl + b
```

---

## `Ctrl + d`

Move half a screen down.

```text
Ctrl + d
```

---

## `Ctrl + u`

Move half a screen up.

```text
Ctrl + u
```

---

# 8. Saving and Exiting

## `:w`

Save the file.

```text
:w
```

---

## `:q`

Quit Vim.

```text
:q
```

---

## `:wq`

Save and quit.

```text
:wq
```

---

## `:x`

Save and quit.

```text
:x
```

---

## `ZZ`

Save and quit from Normal Mode.

```text
ZZ
```

---

## `:q!`

Quit without saving changes.

```text
:q!
```

---

## `:w!`

Force save.

```text
:w!
```

---

## `:wq!`

Force save and quit.

```text
:wq!
```

---

# 9. Deleting Text

## `x`

Delete the character under the cursor.

```text
x
```

---

## `X`

Delete the character before the cursor.

```text
X
```

---

## `dw`

Delete from the cursor to the beginning of the next word.

```text
dw
```

---

## `de`

Delete from the cursor to the end of the word.

```text
de
```

---

## `d$`

Delete from the cursor to the end of the line.

```text
d$
```

---

## `d0`

Delete from the cursor to the beginning of the line.

```text
d0
```

---

## `dd`

Delete the entire current line.

```text
dd
```

---

## `D`

Delete from the cursor to the end of the line.

```text
D
```

---

## `ndd`

Delete multiple lines.

```text
3dd
```

Deletes 3 lines.

Example:

```text
5dd
```

Deletes 5 lines.

---

# 10. Copying Text

In Vim, copying is called **yanking**.

## `yy`

Copy the current line.

```text
yy
```

---

## `nyy`

Copy multiple lines.

```text
3yy
```

Copies 3 lines.

---

## `yw`

Copy a word.

```text
yw
```

---

## `y$`

Copy from the cursor to the end of the line.

```text
y$
```

---

# 11. Pasting

## `p`

Paste after the cursor/current line.

```text
p
```

---

## `P`

Paste before the cursor/current line.

```text
P
```

---

# 12. Undo and Redo

## `u`

Undo the last change.

```text
u
```

---

## `Ctrl + r`

Redo the undone change.

```text
Ctrl + r
```

---

# 13. Repeating Commands

## `.`

Repeats the last change.

```text
.
```

Example:

```text
dd
.
```

The second `.` repeats the deletion.

---

# 14. Searching

## `/`

Search forward.

```text
/text
```

Example:

```text
/Java
```

Press:

```text
Enter
```

---

## `?`

Search backward.

```text
?text
```

Example:

```text
?Java
```

---

## `n`

Go to the next search result.

```text
n
```

---

## `N`

Go to the previous search result.

```text
N
```

---

## `:noh`

Remove search highlighting.

```text
:noh
```

---

# 15. Replacing Text

## `r`

Replace one character.

```text
rX
```

Replaces the current character with `X`.

---

## `cw`

Change the current word.

```text
cw
```

Type the new word and press:

```text
Esc
```

---

## `cc`

Change the entire current line.

```text
cc
```

---

## `C`

Change from the cursor to the end of the line.

```text
C
```

---

## `:s`

Replace the first occurrence in the current line.

```text
:s/old/new/
```

Example:

```text
:s/Java/Python/
```

---

## `:s/g`

Replace all occurrences in the current line.

```text
:s/old/new/g
```

Example:

```text
:s/Java/Python/g
```

---

## `:%s`

Replace text throughout the entire file.

```text
:%s/old/new/g
```

Example:

```text
:%s/Java/Python/g
```

---

## `:%s` with confirmation

Ask before replacing each occurrence.

```text
:%s/old/new/gc
```

---

# 16. Visual Mode

Visual Mode is used to select text.

## `v`

Select characters.

```text
v
```

Move the cursor to select text.

---

## `V`

Select entire lines.

```text
V
```

Move `j` or `k` to select more lines.

---

## `Ctrl + v`

Select a rectangular/block area.

```text
Ctrl + v
```

---

# 17. Operations on Selected Text

After selecting text:

## `d`

Delete selected text.

```text
d
```

---

## `y`

Copy selected text.

```text
y
```

---

## `c`

Change selected text.

```text
c
```

---

## `>`

Indent selected text.

```text
>
```

---

## `<`

Remove indentation.

```text
<
```

---

# 18. Indentation

## `>>`

Indent the current line.

```text
>>
```

---

## `<<`

Remove indentation from the current line.

```text
<<
```

---

## `n>>`

Indent multiple lines.

```text
3>>
```

---

## `n<<`

Remove indentation from multiple lines.

```text
3<<
```

---

# 19. Joining Lines

## `J`

Join the current line with the next line.

```text
J
```

Example:

```text
Hello
World
```

After `J`:

```text
Hello World
```

---

# 20. Opening New Lines

## `o`

Create a new line below.

```text
o
```

---

## `O`

Create a new line above.

```text
O
```

---

# 21. Line Numbers

## `:set number`

Show line numbers.

```text
:set number
```

---

## `:set nonumber`

Hide line numbers.

```text
:set nonumber
```

---

## `:set relativenumber`

Show relative line numbers.

```text
:set relativenumber
```

---

## `:set norelativenumber`

Hide relative line numbers.

```text
:set norelativenumber
```

---

# 22. Multiple Files

## Open multiple files

```bash
vim file1.txt file2.txt
```

---

## `:next`

Go to the next file.

```text
:next
```

---

## `:prev`

Go to the previous file.

```text
:prev
```

---

## `:first`

Go to the first file.

```text
:first
```

---

## `:last`

Go to the last file.

```text
:last
```

---

# 23. Split Windows

## `:split`

Split the window horizontally.

```text
:split
```

---

## `:vsplit`

Split the window vertically.

```text
:vsplit
```

---

## `Ctrl + w`

Used with other keys to move between windows.

```text
Ctrl + w + w
```

Moves to the next window.

---

## `Ctrl + w + h`

Move to the left window.

```text
Ctrl + w + h
```

---

## `Ctrl + w + l`

Move to the right window.

```text
Ctrl + w + l
```

---

## `Ctrl + w + j`

Move to the window below.

```text
Ctrl + w + j
```

---

## `Ctrl + w + k`

Move to the window above.

```text
Ctrl + w + k
```

---

# 24. Terminal Inside Vim

## `:terminal`

Opens a terminal inside Vim.

```text
:terminal
```

---

# 25. Running Shell Commands

## `:!`

Runs a Linux command without leaving Vim.

```text
:!command
```

Example:

```text
:!ls
```

Another example:

```text
:!pwd
```

---

# 26. File Commands Inside Vim

## `:e`

Open another file.

```text
:e filename
```

Example:

```text
:e notes.txt
```

---

## `:saveas`

Save the current file with a different name.

```text
:saveas newfile.txt
```

---

## `:w filename`

Save current content as another file.

```text
:w backup.txt
```

---

# 27. Selecting the Entire File

Go to the beginning:

```text
gg
```

Then:

```text
V
```

Then:

```text
G
```

This selects the entire file.

You can then:

```text
y
```

to copy it, or:

```text
d
```

to delete it.

---

# 28. Useful Number Prefixes

Many Vim commands can be repeated using a number.

```text
5j
```

Move down 5 lines.

```text
5k
```

Move up 5 lines.

```text
5dd
```

Delete 5 lines.

```text
5yy
```

Copy 5 lines.

```text
5x
```

Delete 5 characters.

```text
5w
```

Move forward 5 words.

---

# 29. Important Vim Command Combinations

```text
dw
```

Delete word.

```text
dd
```

Delete line.

```text
yy
```

Copy line.

```text
p
```

Paste.

```text
u
```

Undo.

```text
Ctrl + r
```

Redo.

```text
gg
```

First line.

```text
G
```

Last line.

```text
0
```

Beginning of line.

```text
$
```

End of line.

```text
w
```

Next word.

```text
b
```

Previous word.

```text
x
```

Delete character.

```text
r
```

Replace character.

```text
cw
```

Change word.

```text
cc
```

Change line.

```text
J
```

Join lines.

```text
.
```

Repeat last change.

---

# 30. Vim Save and Exit Cheat Sheet

| Command | Work                |
| ------- | ------------------- |
| `:w`    | Save                |
| `:q`    | Quit                |
| `:wq`   | Save and quit       |
| `:x`    | Save and quit       |
| `ZZ`    | Save and quit       |
| `:q!`   | Quit without saving |
| `:w!`   | Force save          |
| `:wq!`  | Force save and quit |

---

# 31. Vim Movement Cheat Sheet

| Command    | Work                      |
| ---------- | ------------------------- |
| `h`        | Left                      |
| `j`        | Down                      |
| `k`        | Up                        |
| `l`        | Right                     |
| `w`        | Next word                 |
| `b`        | Previous word             |
| `e`        | End of word               |
| `0`        | Beginning of line         |
| `^`        | First non-space character |
| `$`        | End of line               |
| `gg`       | First line                |
| `G`        | Last line                 |
| `10G`      | Go to line 10             |
| `Ctrl + f` | Page down                 |
| `Ctrl + b` | Page up                   |
| `Ctrl + d` | Half page down            |
| `Ctrl + u` | Half page up              |

---

# 32. Vim Editing Cheat Sheet

| Command    | Work                     |
| ---------- | ------------------------ |
| `i`        | Insert before cursor     |
| `I`        | Insert at line beginning |
| `a`        | Insert after cursor      |
| `A`        | Insert at line end       |
| `o`        | New line below           |
| `O`        | New line above           |
| `x`        | Delete character         |
| `dd`       | Delete line              |
| `dw`       | Delete word              |
| `D`        | Delete to line end       |
| `yy`       | Copy line                |
| `yw`       | Copy word                |
| `p`        | Paste after              |
| `P`        | Paste before             |
| `u`        | Undo                     |
| `Ctrl + r` | Redo                     |
| `r`        | Replace character        |
| `cw`       | Change word              |
| `cc`       | Change line              |
| `J`        | Join lines               |
| `.`        | Repeat last change       |

---

# 33. Vim Search Cheat Sheet

| Command          | Work                      |
| ---------------- | ------------------------- |
| `/text`          | Search forward            |
| `?text`          | Search backward           |
| `n`              | Next result               |
| `N`              | Previous result           |
| `:noh`           | Remove highlighting       |
| `:%s/old/new/g`  | Replace all               |
| `:%s/old/new/gc` | Replace with confirmation |

---

# 34. Vim Visual Mode Cheat Sheet

| Command    | Work                |
| ---------- | ------------------- |
| `v`        | Character selection |
| `V`        | Line selection      |
| `Ctrl + v` | Block selection     |
| `y`        | Copy selection      |
| `d`        | Delete selection    |
| `c`        | Change selection    |
| `>`        | Indent              |
| `<`        | Unindent            |

---

# 35. Most Important Vim Commands for ICP

```text
i
I
a
A
o
O
Esc

h
j
k
l
w
b
e
0
^
$
gg
G

x
dd
dw
D
yy
yw
p
P

u
Ctrl + r
.

/
?
n
N

v
V
Ctrl + v

:w
:q
:wq
:q!

:set number
:set nonumber

:s/old/new/
:s/old/new/g
:%s/old/new/g

:!command
```

# 36. Basic Vim Workflow

Open a file:

```bash
vim notes.txt
```

Enter Insert Mode:

```text
i
```

Write your text:

```text
Hello World
This is my Linux note.
```

Return to Normal Mode:

```text
Esc
```

Save:

```text
:w
```

Quit:

```text
:q
```

Or save and quit directly:

```text
:wq
```

# 37. Vim Mode Flow

```text
             ┌──────────────┐
             │  Normal Mode │
             └──────┬───────┘
                    │
       i / a / o / I / A / O
                    ↓
             ┌──────────────┐
             │  Insert Mode │
             └──────┬───────┘
                    │
                   Esc
                    ↓
             ┌──────────────┐
             │  Normal Mode │
             └──────┬───────┘
                    │
                    :
                    ↓
             ┌──────────────┐
             │ Command Mode │
             └──────────────┘
```

# 38. Quick Vim Revision

```text
i       → Insert
Esc     → Normal mode
h       → Left
j       → Down
k       → Up
l       → Right

w       → Next word
b       → Previous word
0       → Line beginning
$       → Line end
gg      → First line
G       → Last line

x       → Delete character
dd      → Delete line
dw      → Delete word
yy      → Copy line
p       → Paste
u       → Undo
Ctrl+r  → Redo
.       → Repeat

/word   → Search
n       → Next result
N       → Previous result

v       → Select characters
V       → Select lines

:w      → Save
:q      → Quit
:wq     → Save + quit
:q!     → Quit without saving
```
