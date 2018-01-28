iswow64 [![Crates.io](https://img.shields.io/crates/v/iswow64.svg)](https://crates.io/crates/iswow64) [![Build status](https://ci.appveyor.com/api/projects/status/yp2y1mpf2dihbm3v?svg=true)](https://ci.appveyor.com/project/WLBF/iswow64)
======

Determines whether the current process is running under WOW64.
## Example:

```rust
extern crate iswow64;

let result = iswow64::iswow64();

println!("{:?}", result);

#[cfg(target_arch = "x86")]
assert_eq!(result.unwrap(), true);

#[cfg(target_arch = "x86_64")]
assert_eq!(result.unwrap(), false);

```