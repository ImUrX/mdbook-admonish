# Chapter 1

```admonish abstract "What <i>is</i> this?"
This book acts as an integration test for `mdbook-admonish`.

It verifies that `mdbook` post-processes our generated HTML in the way we expect.
```

```admonish
Simples
```

```admonish warning ""
No title, only body
```

```admonish title="
No title, only body
```

```admonish collapsible=true
Hidden on load
```

{{#include common_warning.md}}

````admonish
```bash
Nested code block
```
````

````admonish
```rust
let x = 10;
x = 20;
```

```rust
let x = 10;
let x = 20;
```
````
