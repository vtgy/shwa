# Shwa (ə)

"Shellscript with attachments"

## Defense

POSIX shellscript sucks; this is a quick and dirty library that substantially improves its expressive power.

## Caveats

Watch out using lists, never allow the variables you use to store lists be affected directly by user input (i.e. not wrapped in a call to quote) as code can be easily injected into the `eval set --` calls required to dynamically load the lists into the argument array.

## Reference

### `is` `cmd` `...`

Determine if the command `is_$cmd $@` is succesful. Wrapper for the `is_` family of commands.

#### `is_command` `arg`

Check if `arg` succeeds as an argument to `command -V` (checks if it is runnable as a command).

#### `is_name` `arg`

Check if `arg` is a valid name for a variable (POSIX only).

#### `is_natural` `arg`

Check if `arg` is a natural number (only digits).

### `length` `list`

Write the number of items in `list` to stdout.

### `nab` `var`

Write the value of `var` to stdout.

### `peek` `list` `[index]`

Write the element at `index` (default is 0) in `list` to stdout.

### `pop` `list` `var`

Place the first element of `list` into `var` and remove it from `list`.

### `push` `list` `@values`

Place `values` onto the front of `list`.

### `put` `var` `*value`

Set `var` to `value`.

### `lay` `list` `@values`

Set `list` to a properly quoted string of values (which can be expanded to and manipulated as an argument list).

### `queue` `list` `@values`

Place `values` onto the end of `list`.

### `quote` `@values`

Quote `values` to be stored and evaluated safely.
