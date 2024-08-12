# Variables

### Question 1

Which syntax creates a variable that can be reassigned?

A) `let mut x = 99;`

B) `const MINUTES_PER_HOUR = 60;`

C) `let y = 10;`

### Question 2

What will be the output of the following program?

```rust
fn main() {
    let initial_balance = 9;
    let initial_balance = initial_balance - 3;
    {
        let initial_balance = initial_balance * 2;
    }
    println!("Final balance is: {}", initial_balance);
}
```

A) Final balance is: 6. 

B) Final balance is: 12. 

C) The program won't compile.

### Question 3

How to make this program compile?

```rust
fn main() {
    x = 5;
    println!("The value of x is: {}", x);
    x = 6;
    println!("The value of x is: {}", x);
}
```

A) x = 5_u8;

B) let x = 5;

C) let mut x = 5;

### Question 4

What concept applies in this code fragment?

```rust
fn main() {
    let x = 5;
    let x = x + 1;
    {
        let x = x * 2;
        println!("Inner scope x value is: {}", x);
    }
    println!("Outer scope x value is: {}", x);
}
```

A) Mutability

B) Shadowing

C) Constants