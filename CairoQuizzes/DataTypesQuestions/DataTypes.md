### Question #1

The largest number representable by the type `i128` is:

A) 2^127

B) 2^128

C) 2^127 - 1

Correct answer: C

Justification: In general, a **signed** number with *n* bits can represent numbers between -(2^n - 1) and 2^n-1 - 1. For **unsigned** numbers the range is from 0 to 2^n - 1.

### Question #2

If `x : u8 = 0`, what will happen when computing `x - 1`?

A) It will return `-1`

B) It will always panic.

C)

Correct answer: B

Justification: `u8` is an unsigned integer type which cannot contain negative numbers.