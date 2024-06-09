# Shwa (ə)

"Shellscript with attachments"

## Defense

POSIX shellscript sucks; this is a quick and dirty library that substantially improves its expressive power.

## Caveats

Watch out using lists, never allow the variables you use to store lists be affected directly by user input (i.e. not wrapped in a call to quote) as code can be easily injected into the `eval set --` calls required to dynamically load the lists into the argument array.

# Reference

## `basename` `path` `[suffix]`

Calculate the immediately relative name of `path` (with optional removal of `suffix`.)

## `bsf` `path`

Pass if `path` is a block-special file.

## `count` `@items`

Write `$#` to standard output.

## `csf` `path`

Pass if `path` is a character-special file.

## `decimal` `argument`

Pass if `argument` is a decimal number.

## `default` `@commands`

Write first of `commands` to succeed as argument to `has`. Useful for determining available dependency options automatically.

## `dirname` `path`

Calculate the path of the directory containing `path`.

## `directory` `path`

Pass if `path` is a directory.

## `empty` `path`

Pass if `path` is empty.

## `err` `@lines`

Write `lines` to standard error.

## `executable` `path`

Pass if `path` is executable.

## `exists` `path`

Pass if `path` is a file.

## `fifo` `path`

Pass if `path` is a FIFO (named pipe.)

## `get` `name`

Write value of variable `name` to standard output.

## `has` `command`

Pass if `command` is available.

## `integer` `argument`

Pass if `argument` is an integer.

## `lay` `list` `@items`

Assign variable `list` to quoted `items`.

## `length` `list`

## `match` `pattern` `argument`

## `name` `argument`

## `natural` `argument`

## `null` `argument`

## `out` `@lines`

## `peek` `list` `[index=0]`

## `pop` `list` `variable`

## `printfq` `format` `argument`

## `push` `list` `@items`

## `put` `name` `*value`

## `qat`

## `queue` `list` `@items`

## `quote` `@items`

Wrap each of `items` in evaluation-safe quoting and write them to standard output in a single, space-seperated line.

This is a highly powerful operation that enables all further list operations.

If no items are provided, they will be read line-by-line from standard input.

## `readable` `path`

## `regular` `path`

## `same` `@items`

## `sgid` `path`

## `socket` `path`

## `suid` `path`

## `symlink` `path`

## `terminal` `[fd=0]`

## `writeable` `path`
