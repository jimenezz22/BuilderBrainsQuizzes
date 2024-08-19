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

### Question #3

Determine whether the program will pass the compiler. If it passes, write the expected output of the program if it were executed.

```rust
fn main() {
  let x: felt32 = 2;
  println!("{x}");
}
```

A) This program **does not** compile.

B) This program **does** compile.

C) The output of this program will be x

Correct answer: A

Justification: The type `felt32` does not exist. Proper field type is `felt252`

### Question #4

Which of the following statements is correct regarding the felt252 type in Cairo?

A) `felt252` is a 252-bit integer type, used to represent negative and positive numbers.

B) `felt252` es un tipo especial que representa elementos de campo, donde los valores se encuentran en un rango específico determinado por un número primo grande.

C) `felt252` es un tipo flotante similar a `f32` o `f64` en otros lenguajes de programación.

Correct answer: B

Justification: