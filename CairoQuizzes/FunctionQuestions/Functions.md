### Question #1

The keyword for declaring a new function in Cairo is:

A) fn

B) pub fn

C) let fn

Correct answer: A

Justification:

### Question #2

Determine whether the program will pass the compiler. If it passes, write the expected output of the program if it were executed.

```rust
fn f(x) { 
  println!("{x}");
}
fn main() {
  f(0);
}
```

This program: 

A) Does compile

B) Does not compile

C) Does compile with warnings

Correct answer:

Justification:

### Question #3

In Cairo, a curly-brace block like { /* ... */ } is:

A) An expression
B) A statement
C) A syntactic scope

A) 2 only

B) 1 only

C) 2 and 3

D) 1 and 3

Correct answer:

Justification:

### Question #4

Determine whether the program will pass the compiler. If it passes, write the expected output of the program if it were executed.

```rust
fn f(x: usize) -> usize { x + 1 }
fn main() {
  println!("{}", f({
    let y = 1;
    y + 1
  }));
}
```

This program: 

A) Does compile

B) Does not compile

C) Does compile with warnings

Correct answer:

Justification: