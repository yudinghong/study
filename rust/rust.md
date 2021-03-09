# Rust

## cargo 
> cargo new xxx 
cargo build (--release)
cargo run (--release)
cargo clippy (like eslint)
cargo tree (check dependency)
cargo bench (run benchmark)
cargo udeps (check unused packages)

## grammar
```rust
fn main(){
  println!("hello {}, {0}, {1}, {{}}", "world", "hh");
}
```
```rust
let a = 123;
// wrong
a = "abc"; // a is int when define
a = 4.56; // can't convert with precision loss
a = 456; // a is a immutable variable
// right
let mut a = 123;
a = 456;
// or 
let a = 123;
let a = 345;
// it's wrong when a is constant
const a: i32 = 123;// wrong
let a = 345;
// declare type
let a :u64 = 123;
// shadowing, the diffence between shadowing and deassign is that the shadowing can reuse the variable, deassign can't change the type of variable 
let x = 5;
let x = x + 1;
let x = x * 2;
// data type
/*
i8 u8
i16 u16
i32 u32
i64 u64
i128 u128
isize usize
int example:
98_222  eq  98222
0xff
0o77
0b111_10
b'A' just byte
*/

```
