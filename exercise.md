# (Neo)Vim

Vim and Neovim are powerful, modal text editors known for efficiency and customization. Vim is
widely used with a steep learning curve, while Neovim is a modernized fork with improvements in
maintainability and extensibility. Both are popular among developers for their speed, flexibility,
and robust feature sets.

---

### Change

`c` is a powerful motion. You use it just like `d` but at the end of the
motion you are ejected from `NORMAL` and into `INSERT`.

So if you wished to delete a word and then type in a new word, `c` is a great
habit to form.

Lets see the difference

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
