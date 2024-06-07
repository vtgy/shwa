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

### `are_different` `@values`

### `are_same` `@values`

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

### `is_block` `value`

### `is_character` `value`

### `is_decimal` `value`

### `is_directory` `value`

### `is_empty` `value`

### `is_executable` `value`

### `is_fifo` `value`

### `is_file` `value`

### `is_integer` `value`

### `is_name` `value`

### `is_natural` `value`

### `is_null` `value`

### `is_readable` `value`

### `is_regular` `value`

### `is_sgid` `value`

### `is_socket` `value`

### `is_symlink` `value`

### `is_suid` `value`

### `is_terminal` `value`

### `is_writeable` `value`

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
