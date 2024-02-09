# (Neo)Vim

Vim and Neovim are powerful, modal text editors known for efficiency and customization. Vim is
widely used with a steep learning curve, while Neovim is a modernized fork with improvements in
maintainability and extensibility. Both are popular among developers for their speed, flexibility,
and robust feature sets.

---

## (Neo)Vim: the Text Editor

(Neo)Vim is just a text editor, when people say "I use Vim", most of the time, they meant `Vim Motion`.

While you can get a GUI for it, the binary is meant to be executed in a terminal emulator.
Should you move on and become a software dev/engr, (likely) at one point, you will have to `ssh`
into a remote server and make some changes using Vim.

For day-to-day usage, I use Neovim, and for the rest of the workshop, we will be focusing more on NeoVim,
but the **vim motion** is the same, and personally I find Lua is a lot easier to read than VimScript.

Like other modern text editor, Neovim is customizable, has native support for Language Server Protocol,
code completion, diagnostics, snippets, and a lot of community support, plugins, and rich ecosystem.

```
:help config
```

## Vim Motion

Vim motion is the true power, it can be a lot at first, but it is surprisingly straight forward:

### Modes

- `NORMAL`
- `INSERT`
- `VISUAL`
- `COMMAND`

### Basic motion

left down up right with `hjkl`

#### `action`

Delete a line with `dd`. It then saves it to a clipboard buffer
(think \<C-x>, or `Cut`).

To `paste`, <d>

##### Example:

Delete this line

#### `count` `action`

Number of times you want to do an action, and what action you are doing.

`2dd`, `3dd` ...

##### Example:

Delete this line 1\
Delete this line 2\
Delete this line 3

#### `count` `action` `direction`

Number of times you want to do an action, and what action you are doing, then what direction are you going?

`3dj`

##### Example:

Delete this line 1\
Delete this line 2\
Delete this line 3

## Exercises:

sauce:
https://raw.githubusercontent.com/ThePrimeagen/vim-fundamentals/master/course-website/lessons/exercise-6-motions.md

### Change

`c` is a powerful motion. You use it just like `d` but at the end of the
motion you are ejected from `NORMAL` and into `INSERT`.

So if you wished to delete a word and then type in a new word, `c` is a great
habit to form.

Let's see the difference

// dd this line
// cc this line

### Horizontal Movement

Lets learn about!: `_`, `0`, `$`, `D`, `C`, `S`, `f`, `,`, `;`, `t`, `F`, and `T`

// How would we move around on the line with "contents"
if (true) {
contents conTenTs contenTS
}

### Vertical Movement

#### Core movement

Rely on relative jumps. Get good at them.

If you get NeoVim, try VimBeGood

#### { and }

We know about search. That is a vertical movement, but its really specific.

First lets talk `{` and `}`

ContiguousCode
ContiguousCode
ContiguousCode
ContiguousCode
ContiguousCode
ContiguousCode
ContiguousCode

ContiguousCode
ContiguousCode
ContiguousCode
ContiguousCode
ContiguousCode
ContiguousCode
ContiguousCode

This next one is a bit odd

#### Ctrl+u/d

So let's do another type of navigation.

Try pressing `<C-d>`

.

.
.

.

.

.

.

.

.

.

.

.

.

.

.

.

.

.

.

.

.

.

.

.

.

#### \]m and \]M

This will move by "function". It works pretty well in c languages.

Move your cusor to this line and press `]m`. Try moving back and forth and try
the uppercase version as well.

if (foo) {
some content
some content
some content
some content
function bar() {
some other content
some other content
some other content
some other content
}
function baz() {
other content
other content
other content
other content
}
}

#### %

Ok,.... soo this isn't a pure vertical motion. It actually is a pair jumper

if (true) {
content
const a = \[
content,
content,
content,
\]

```
"content"

content
content
```

}

Lets combine it with a motion. Delete the `const a =...` statement.

Lets look at the following statement, what are some ways you can delete the
contents of the if statement?

if (true) {
line1
line2
line3
line4
line5
}

So lets try again..

if (true) {
line1
// Some distance
line2
line3

```
line4
line5
```

}
