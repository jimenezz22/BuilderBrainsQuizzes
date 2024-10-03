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

Correct answer: D) 

Justification: In Cairo, as in Rust, a curly-brace block is both an expression (it can evaluate to a value) and defines a syntactic scope. It can be used to define a scope in which variables are valid only inside the block, and it can also return a value from that scope, making it an expression​​.

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

Correct answer: A

Justification: This program compiles successfully because the block { let y = 1; y + 1 } is an expression that evaluates to 2, which is then passed as the argument to f. The function f adds 1 to this value, resulting in 3 being printed. The block in the println! call is valid and returns a value that can be passed to f

### Question #5

Does the following program compile correctly? If so, indicate the expected result if executed.

```rust
fn double_value(x: usize) -> usize {
    x * 2
}

fn main() {
    let z = {
        let a = 10;
        a + 5
    };

    println!("{}", double_value(z));
}
```

This program:

A) Yes it compiles

B) Does not compile

C) Compile with warnings

Correct answer: A

Justification: The block { let a = 10; a + 5 } is a valid expression that evaluates to 15. This value is assigned to z, which is then passed as an argument to the double_value function, which returns double the value (30 in this case). The program will print 30 without compilation errors​.