# riscv_insn_decode

if you want to you use `riscv_insn_decode`,you need add this lib to `Cargo.toml`

```toml
[dependencies]
riscv_insn_decode = {git = "https://github.com/hm1229/riscv_insn_decode", rev = "0b954c9"}
```

## Structs

### InsnStatus

to show instruction is legal or not

```rust
#[derive(Debug)]
pub enum InsnStatus {
    Illegal,
    Legal,
}
```

## APIs

### get_insn_length

give the address of the instruction, and it will return the length of it.

```rust
use riscv_insn_decode::get_insn_length;

let length = get_insn_length(addr);
```

### insn_decode

give the address of the instruction, and it will return the legitimacy of it.

```rust
use riscv_insn_decode::{insn_decode, InsnStatus};

match insn_decode(addr){
    InsnStatus::Legal => {
        unimplemented!();
    },
    InsnStatus::Illegal => {
        unimplemented!();
    }
}
```

