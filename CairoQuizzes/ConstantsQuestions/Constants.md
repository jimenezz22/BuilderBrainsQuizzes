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

### Question #3

What value does the first element of the BOOL_FIXED_SIZE_ARRAY constant contain?

```rust
const ONE_HOUR_IN_SECONDS: u32 = 3600;
const STRUCT_INSTANCE: AnyStruct = AnyStruct { a: 0, b: 1 };
const ENUM_INSTANCE: AnyEnum = AnyEnum::A('any enum');
const BOOL_FIXED_SIZE_ARRAY: [bool; 2] = [true, false];
```

A) `false`

B) `true`

C) `null`

Correct answer: B

### Question #4

What type of data does the ENUM_INSTANCE constant have in the example code?

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

A) AnyStruct

B) AnyEnum

C) felt252

Correct answer: B

### Question #5

In Cairo, constants are always immutable and must be declared using the `const` keyword. Considering the restrictions and characteristics of constants in Cairo, which of the following statements is correct and what is its technical justification?

A) Constants in Cairo can be declared anywhere in the code, even within functions, as long as the variable scope rules are respected.

B) Las constantes en Cairo pueden ser inicializadas con valores calculados en tiempo de ejecución si dichos cálculos no modifican el valor después de la inicialización.

C) Las constantes en Cairo deben ser declaradas en el ámbito global y solo pueden ser inicializadas con expresiones constantes, no con resultados de cálculos en tiempo de ejecución.

Correct answer: C

Justification: Constants in Cairo, being immutable and declared in the global scope, must have a value defined at compile time. This ensures that they do not depend on runtime calculations, improving security and allowing compiler optimizations, guaranteeing a predictable value throughout the program.