### Question #1

The keyword for declaring a new function in Cairo is:

A) fn

B) pub fn

C) let fn

Correct answer: A

Justification: In Cairo, functions are declared using the fn keyword, similar to Rust. The keyword pub is used to denote public functions, but fn alone is used to declare a function in its basic form​.

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

Correct answer: B

Justification: The function f is missing a type annotation for the parameter x. In Cairo (as in Rust), all function parameters must have explicitly defined types. Since the type of x is not specified in fn f(x), this would lead to a compilation error​.

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