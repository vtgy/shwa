# Shwa (ə)

"Shellscript with attachments"

## Defense

POSIX shellscript sucks; this is a quick and dirty library that substantially improves its expressive power.

## Caveats

Watch out using lists, never allow the variables you use to store lists be affected directly by user input (i.e. not wrapped in a call to quote) as code can be easily injected into the `eval set --` calls required to dynamically load the lists into the argument array.

# Reference

## `@`

Alias for `set --`. Shorthand symmetric with array variable (`$@`).

## `are` `subcommand` `@values`

### `different`

### `same`

## `arent` `subcommand` `@values`

## `count` `@items`

## `basename` `path` `[suffix]`

## `default` `@commands`

## `dirname` `path`

## `err` `@lines`

## `fail`

Alias for `return 1`.

## `get` `variable`

## `has` `command`

## `hasnt` `command`

## `is` `subcommand` `value`

### `block`

### `character`

### `decimal`

### `directory`

### `empty`

### `executable`

### `fifo`

### `file`

### `integer`

### `name`

### `natural`

### `null`

### `readable`

### `regular`

### `sgid`

### `socket`

### `symlink`

### `suid`

### `terminal`

### `writeable`

## `isnt` `subcommand` `value`

Synonym for `! is`.

## `lay` `list` `@items`

## `length` `list`

## `out` `@lines`

## `pass`

Alias for `return 0`.

## `peek` `list` `[index]`

## `pop` `list` `variable`

## `printfq` `format` `*value`

## `put` `variable` `*value`

## `push` `list` `@items`

## `qat`

## `queue` `list` `@items`

## `quote` `@items`
