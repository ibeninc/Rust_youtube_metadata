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



## Limitations

- This library won't be able to fetch `audiostreams` and `videostreams` for unpopular videos, because YouTube does not generate separate streams for unpopular videos. However, it will still be able to fetch normal `streams`.

- Since this library does not depend on [youtube-dl](https://github.com/rg3/youtube-dl), there are some more things (not mentioning here) that we'll be missing out.

## Running Tests

```
$ cargo test
```
