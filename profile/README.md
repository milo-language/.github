## Milo

A memory-safe systems language that compiles to LLVM IR. No GC, no reference counting, no lifetime annotations.

### **[milo-language.github.io/milo →](https://milo-language.github.io/milo/)**

[Tour](https://milo-language.github.io/milo/tour) ·
[Install](https://milo-language.github.io/milo/getting-started/installation) ·
[Language reference](https://milo-language.github.io/milo/language/) ·
[Built with Milo](https://milo-language.github.io/milo/demos)

```milo
fn main(): i32 {
    print("Hello, Milo!")
    return 0
}
```

Ownership and move semantics catch use-after-move and use-after-free at compile time. References are second-class: `&T` appears in function parameters and nowhere else, so there is no lifetime algebra to learn. Cyclic data lives in an arena behind generational handles.

### Built with it

<p align="center">
  <img src="https://raw.githubusercontent.com/milo-language/milo/main/docs/site/public/showcase/nes.png" alt="Super Mario Bros. 3 running on the Milo NES emulator" width="30%">
  <img src="https://raw.githubusercontent.com/milo-language/milo/main/docs/site/public/showcase/genesis.png" alt="Sonic the Hedgehog running on the Milo Genesis emulator" width="30%">
  <img src="https://raw.githubusercontent.com/milo-language/milo/main/docs/site/public/showcase/snes.png" alt="Super Mario World running on the Milo SNES emulator" width="30%">
</p>

The compiler self-hosts: a Milo-written Milo compiler reaches a byte-identical fixed point across three bootstrap stages.

Beyond that — emulators that play commercial games natively and in the browser; a JavaScript engine and runtime; a DAP debugger with a React front end; a TUI framework; HTTP servers and clients over a certificate-verifying TLS layer; and firmware for bare-metal Cortex-M.

The standard library ships a contract prover written in Milo. It discharges stdlib preconditions in CI, and a contract proven false fails the build.

### Repositories

| Repo | Contents |
| --- | --- |
| [milo](https://github.com/milo-language/milo) | Compiler, standard library, docs, examples |
| [emulators](https://github.com/milo-language/emulators) | NES, SNES, and Genesis cores plus a console front-end |
| [milojs](https://github.com/milo-language/milojs) | A JavaScript engine and runtime, no JSC and no V8 |
| [dapweb](https://github.com/milo-language/dapweb) | Web and AI interface for any DAP debugger |

Each ships prebuilt binaries for macOS and Linux on its releases page.
