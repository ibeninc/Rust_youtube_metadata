# Rust youtube metadata downloader


Rust package to fetch YouTube metadata.

## Installation

Put the below in your `Cargo.toml`

> [dependencies]
>
> rafy = "0.2"

## Examples

```rust
extern crate rafy;
use rafy::Rafy;

fn main() {
    let content = Rafy::new("https://www.youtube.com/watch?v=DjMkfARvGE8").unwrap();
    println!("{}", content.videoid);
    println!("{}", content.title);
    println!("{}", content.rating);
    println!("{}", content.viewcount);
}
```


