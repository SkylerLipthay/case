# case

This is a set of letter case string helpers.

## Installation

If you're using Cargo, just add `case` to your `Cargo.toml`:

```toml
[dependencies]
case = "0.0.1"
```

## Usage

```rust
extern crate case;

use case::CaseExt;

// Snake case operations:
assert_eq!(&"a_string_and_a_miss".to_camel(), "AStringAndAMiss");
assert_eq!(&"string_henry_iii".to_camel_lowercase(), "stringHenryIii");
assert_eq!(&"stringing_in_the_rain".to_dashed(), "stringing-in-the-rain");

// Camel case operations:
assert_eq!(&"martinLutherStringJr".to_snake(), "martin_luther_string_jr");

// Universal operations:
assert_eq!(&"stringy string".to_capitalized(), "Stringy string");
```

## To-do

* `to_human`/`to_human_lowercase`: convert underscores to spaces and optionally capitalize the
  first character
* `to_title`: convert underscores to spaces and capitalize each word's first character
