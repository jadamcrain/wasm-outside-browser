---
marp: true
theme: gaia
class:
  - lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
footer: 'Battalion Energy | June 10th, 2025'
---

# WebAssembly Outside the Browser

**Adam Crain**
*June 10th, 2025*

---

# Agenda

- TODO

---

# "Portable Assembly"

- **Stack-based virtual machine**: Low-level bytecode
- **Language agnostic**: Compile from C/C++, Rust, Go, C#, etc.
- **Portable**: Write once, run anywhere (browsers, servers, edge, etc)
- **Small & fast**: Compact binary format, fast startup times

---
<!-- footer: "" -->

### "BYTE CODE"
### "VIRTUAL MACHINE"
### "WRITE ONCE, RUN ANYWHERE"


![bg right width:600px](./static/duke_blurred.png)

---
<!-- footer: "" -->
# NOPE

![bg right width:600px](./static/duke_revealed.png)

---

# Why?!

- **JavaScript limitations**: Dynamic typing, JIT compilation overhead
- **Need for true bytecode**: Faster parsing, smaller payloads, predictable performance
- **Cross-language support**: Run C/C++/Rust/Go code in browsers efficiently
- **Sandboxed**: Memory-safe, capability-based security model

---

# WASM History

- **2015**: WebAssembly first announced by Mozilla, Google, Microsoft, Apple
- **2017**: MVP (Minimum Viable Product) shipped in all major browsers
- **2019**: W3C standardization - became official web standard
- **2020+**: WASI (WebAssembly System Interface) enables non-browser environments

---

# Simplest WASM Binary

```rust
#[unsafe(no_mangle)]
pub extern "C" fn add(a: i32, b: i32) -> i32 {
  a + b
}
```

```bash
> cargo build --release --target wasm32-unknown-unknown
```

```bash
> ls -ls /target/wasm32-unknown-unknown
4 -rwxrwxr-x 2 jadamcrain jadamcrain  400 Jun 10 10:42 no_std_wasm.wasm
```

400 bytes!

---

# What's inside?

```bash
> wasm-tools print target/wasm32-unknown-unknown/no_std_wasm.wasm
```

```wasm
(module $no_std_wasm.wasm
  (type (;0;) (func (param i32 i32) (result i32)))
  < ... omitted ...>
  (func $add (;0;) (type 0) (param i32 i32) (result i32)
    local.get 1
    local.get 0
    i32.add
  )
  < ... omitted ...>
)
```
---

# Conclusion

## Summary of key points

1. **Main takeaway 1**
2. **Main takeaway 2** 
3. **Main takeaway 3**

---

# Questions?

## Thank you for your attention!

**Contact Information:**
- Email: your.email@example.com
- GitHub: @yourusername
- LinkedIn: /in/yourprofile

---

<!-- _class: lead -->

# Backup Slides

Additional content that might be useful during Q&A

---

# Additional Resources

- [Marp Documentation](https://marp.app/)
- [Marp Themes](https://github.com/marp-team/marp-core/tree/main/themes)
- [Markdown Guide](https://www.markdownguide.org/)