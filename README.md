# shwa

"Shell With Attachments"

## Defense

POSIX shellscript sucks; this is a quick and dirty library that substantially improves its expressive power.

## Caveats

Watch out using lists, never allow the variables you use to store lists be affected directly by user input (i.e. not wrapped in a call to quote) as code can be easily injected into the `eval set --` calls required to dynamically load the lists into the argument array.

