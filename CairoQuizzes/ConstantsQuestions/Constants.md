# Constans

### Question 1

Which of the following statements is correct regarding the constants in Cairo?

A) Constants in Cairo can be declared with the let keyword and are always mutable.

B) Constants in Cairo can be assigned to values that are calculated at run time.

C) Constants in Cairo must be declared with the const keyword and their data type must be noted.

Correct answer: C

### Question #2

Using the code below as example

```rust
struct AnyStruct {
    a: u256,
    b: u32
}

enum AnyEnum {
    A: felt252,
    B: (usize, u256)
}

const ONE_HOUR_IN_SECONDS: u32 = 3600;
const STRUCT_INSTANCE: AnyStruct = AnyStruct { a: 0, b: 1 };
const ENUM_INSTANCE: AnyEnum = AnyEnum::A('any enum');
const BOOL_FIXED_SIZE_ARRAY: [bool; 2] = [true, false];
```

Which of the following statements is correct about the STRUCT_INSTANCE constant in the example code?

A) STRUCT_INSTANCE is an instance of an enum type.

B) STRUCT_INSTANCE is an instance of a structure with two fields, a of type u256 and b of type u32.

C) STRUCT_INSTANCE is an array of boolean values.

Correct answer: B