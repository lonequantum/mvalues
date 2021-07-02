# mvalues
Math Values Generator  
1.0.1

Outputs a series of values with user-defined *start* and *end*. The difference of successive values follows the specified *mode*.

TESTED WITH GNU BC (IN POSIX MODE) ONLY

Calling the mvalues script without argument displays this help:
```
Generates a list of math values, one per line.
This script uses bc internally.

Usage:
mvalues constant|linear|sine {specific mode args}

Examples:
mvalues constant 8.2 14        # 8.2, 14 times. Also accepts any string that must be repeated.
mvalues linear 86 81.1 7       # 7 equally separated values from 86 to 81.1 (bounds included).
mvalues sine 45 180 15 10 a 9  # sin(x) scaled to a series that starts at 15 and ends at 10 (with a peak that is (a)utomatically computed in this case), for 9 equally separated values of x from 45 to 180 degrees (bounds included).

Environment:
MVALUES_ROUND: output precision (maximum number of digits after the decimal point)
               if >= 0, the values will be rounded (to the nearest)
               if  < 0, the values will be truncated after -MVALUES_ROUND digits
               default = 3, max = 66, min = -66
```

## TODO

- Test under other OSes such as \*BSD.
- Add other variations modes (+ support custom functions?).
- Add more checks on input.
- Currently this aims to be a POSIX shell script, perhaps it would be good to rewrite this project in C.
