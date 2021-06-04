# mvalues
Math values generator

More precisely, it outputs a series of values with a user-defined start and end. The spacing of successive values follows a specified mode.  
THIS IS A WORK IN PROGRESS AND THE API IS NOT STABLE YET

Calling the mvalues script without argument displays this help:
```
Generates a list of math values, one per line.
This script uses bc internally.

Usage:
mvalues constant|linear|sine {specific mode args}

Examples:
mvalues constant 8.2 14              # 8.2, 14 times. Also accepts any string that must be repeated.
mvalues linear 86 81.1 7             # 7 equally separated values from 86 to 81.1 (bounds included).
mvalues linear 1.02 44.055 7         # Idem in [1.02, 44.055].
mvalues sine tau/8 tau/2 15 10 a 19  # sin(x) scaled to a series that starts at 15 and ends at 10 (with a peak that is (a)utomatically computed), for 19 equally separated values of x from tau/8 to tau/2 (bounds included).

Environment:
SCALE: setter for bc's scale variable, default = 3.
```

## TODO
- Currently this is a POSIX shell script, perhaps it would be good to rewrite this project in C.
- Add support for custom functions.
- Add more checks on input.
