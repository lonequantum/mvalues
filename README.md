# mvalues
Math values generator
More precisely, it outputs a series of values whose calculation involves a specified range.

Calling the mvalues script without argument displays this help:
```
Generates a list of math values, one per line.
This script uses bc internally.

Usage:
mvalues constant|linear|sine {specific mode args}

Examples:
mvalues constant 8.2 14            # 8.2, 14 times. Also accepts any string that must be repeated.
mvalues linear 86 81.1 7           # 7 equally separated values from 86 to 81.1 (bounds included).
mvalues linear 1.02 44.055 7       # Idem from 1.020 to 44.055.
mvalues sine tau/8 tau/2 5 4.8 19  # sin(x) * 5 + 4.8, for 19 equally separated values of x from tau/8 to tau/2 (bounds included).

Environment:
SCALE: setter for bc's scale variable, default = 3.
```

## TODO
- Currently this is a POSIX shell script, perhaps it would be good to rewrite this project in C.
- Add support for custom functions.
- Add more checks on input.
