# kak-move-lines

A plugin for the [kakoune](https://kakoune.org) text editor that allows you to
easily move your selected lines up and down.

## Installation

Source `move-lines.kak` in your `kakrc`, or use a plugin manager.

## Usage

The plugin provides the `move-lines-up` and `move-lines-down` commands. Intended
use is to bind these commands to keys in normal mode:

```
map global normal <c-s-j> ': move-lines-down %val{count}<ret>'
map global normal <c-s-k> ': move-lines-up %val{count}<ret>'
```

Note the use of single quotes and `%val{count}`. This allows you to optionally
specify the number of lines to move by - `<c-s-j>` will move down one line, but
`15<c-s-j>` will move down 15 lines.

## Contributing

Please send questions, bug reports, patches, etc. to the
[mailing list](https://lists.sr.ht/~raiguard/public-inbox).
