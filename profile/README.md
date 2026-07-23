## Milo

A memory-safe systems language that compiles to LLVM IR. No GC, no reference counting, no lifetime annotations.

```milo
fn main(): i32 {
    print("Hello, Milo!")
    return 0
}
```

Ownership and move semantics catch use-after-move and use-after-free at compile time. References are second-class: `&T` appears in function parameters and nowhere else, so there is no lifetime algebra to learn. Cyclic data lives in an arena behind generational handles.

### Repositories

| Repo | Contents |
| --- | --- |
| [milo](https://github.com/milo-language/milo) | Compiler, standard library, docs, examples |

### Built with it

The compiler self-hosts. A Milo-written Milo compiler reaches a byte-identical fixed point across three bootstrap stages.

Beyond that: NES, SNES, and Genesis emulators that play commercial games natively and in the browser; a JavaScript engine and a Node-compatible runtime; a DAP debugger with a React front end; a TUI framework; HTTP servers and clients over a certificate-verifying TLS layer; and firmware for bare-metal Cortex-M.

The standard library ships a contract prover written in Milo. It discharges stdlib preconditions in CI, and a contract proven false fails the build.

[Documentation](https://milo-language.github.io/milo/) · [Tour](https://milo-language.github.io/milo/tour) · [Install](https://milo-language.github.io/milo/getting-started/installation) · [Built with Milo](https://milo-language.github.io/milo/demos)
