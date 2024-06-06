# Shwa (ə)

"Shellscript with attachments"

## Defense

POSIX shellscript sucks; this is a quick and dirty library that substantially improves its expressive power.

## Caveats

Watch out using lists, never allow the variables you use to store lists be affected directly by user input (i.e. not wrapped in a call to quote) as code can be easily injected into the `eval set --` calls required to dynamically load the lists into the argument array.

## Reference

### `argc` `@args`

Write number of `args` to stdout.

### `is` `cmd` `...`

Determine if the command `is_$cmd $@` is succesful. Wrapper for the `is_` family of commands.

Below are all of the `is_` commands as defined directly by shwa. Obviously users may define their own commands
with the same naming scheme as to extend the functionality of `is`.

#### `command`

If a valid (known) command.

#### `name`

If a valid name.

#### `natural`

If consisting entirely of digits.

#### `decimal`

If a valid rational number (typed out in decimal form).

#### `integer`

If an integer (natural with an optional sign).

#### `block`

Same as `test -b`.

#### `character`

Same as `test -c`.

#### `directory`

Same as `test -d`.

#### `file`

Same as `test -e`.

#### `regular`

Same as `test -f`.

#### `sgid`

Same as `test -g`.

#### `symlink`

Same as `test -h`.

#### `fifo`

Same as `test -p`.

#### `readable`

Same as `test -r`.

#### `nonempty`

Same as `test -s`.

#### `empty`

Same as `! test -s`.

#### `terminal`

Same as `test -t`.

#### `suid`

Same as `test -u`.

#### `writeable`

Same as `test -w`.

#### `executable`

Same as `test -x`.

#### `socket`

Same as `test -S`.

#### `zero`

Same as `test -z`.

#### `nonzero`

Same as `test -n`.

#### `same`

If all arguments are the same.

#### `different`

If all arguments are different.

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

### `printfq` `fmt` `*value`

Will execute `printf` on the given format and quote-wrapped value. Used by `quote`.

### `lay` `list` `@values`

Set `list` to a properly quoted string of values (which can be expanded to and manipulated as an argument list).

### `queue` `list` `@values`

Place `values` onto the end of `list`.

### `quote` `@values`

Quote `values` to be stored and evaluated safely.
