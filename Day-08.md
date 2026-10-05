# Day 8: The Editor's Lair: Mastering Text Editing with VIM

## Entering Execute Mode

Execute Mode allows you to run commands for file operations, searching, and other advanced functionalities. To enter Execute Mode, press:

```bash
:
```

### Practical:

1. Open Vim:

```bash
vim example.txt
```

2. Enter Execute Mode and save the file:

```bash
:w
```

3. Quit Vim:

```bash
:q
```

4. Combine commands to save and quit:

```bash
:wq
```

## Executing Basic Commands: File Operations, Searching, Line Numbering

### File Operations

* Save the file:

```bash
:w
```

* Save as a new file:

```bash
:w newfile.txt
```

* Quit Vim:

```bash
:q
```

* Force quit without saving:

```bash
:q!
```

### Searching

* Search for a term:

```bash
/search_term
```

* Search backward:

```bash
?search_term
```

* Navigate search results:

  * Next occurrence: `n`
  * Previous occurrence: `N`

### Line Numbering

* Show line numbers:

```bash
:set number
```

* Hide line numbers:

```bash
:set nonumber
```

### Practical:

1. Search for the term "example" in a file.
2. Enable line numbering and locate specific lines.

## Entering Visual Mode

Visual Mode allows for text selection and manipulation. To enter Visual Mode, press:

* Character-wise selection:

```bash
v
```

* Line-wise selection:

```bash
V
```

* Block selection:

```bash
Ctrl + v
```

### Practical:

1. Open a file in Vim.
2. Use `v` to select a word or character sequence.
3. Use `V` to select a full line.
4. Use `Ctrl + v` to select a rectangular block of text.

## Manipulating Text in Visual Mode

Once text is selected in Visual Mode, you can manipulate it:

* Copy text:

```bash
y
```

* Delete text:

```bash
d
```

* Paste text:

```bash
p
```

* Replace selected text:

  1. Select the text.
  2. Press `c` to clear and enter Insert Mode.
  3. Type the replacement text and press `Esc`.
