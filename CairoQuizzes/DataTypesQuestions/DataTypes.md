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

### Question #5

What will be the result of the next conversion in Cairo?

```rust
fn main() {
    let x: felt252 = 10;
    let y: u8 = x.try_into().unwrap();
    println!("El valor de y es: {}", y);
}
```

A) The value of y will be 10.

B) The code will throw a conversion error if `x` is greater than `u8::MAX`

C) El valor de `y` será truncado a 8 bits, con un valor final de 2

Correct answer: A

Justification: The value`10` fits within the range of a `u8`, so the conversion is successful and `y` takes the value `10`

### Question #6

What is Cairo's behavior when attempting a safe conversion with try_into and the conversion fails?

A) The conversion fails silently and returns a default value.

B) The conversion returns a `Result` or `Option`, and the error must be handled to avoid a runtime panic.

C) Cairo allows the conversion, but throws a warning instead of an error.

Correct answer: B

Justification: