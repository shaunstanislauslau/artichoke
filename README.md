# Artichoke Ruby

[![CircleCI](https://circleci.com/gh/artichoke/artichoke.svg?style=svg)](https://circleci.com/gh/artichoke/artichoke)
[![Discord](https://img.shields.io/discord/607683947496734760)](https://discord.gg/QCe2tp2)
<br>
[![Core documentation](https://img.shields.io/badge/docs-artichoke--core-blue.svg)](https://artichoke.github.io/artichoke/artichoke_core/)
[![Virtual filesystem documentation](https://img.shields.io/badge/docs-artichoke--vfs-blue.svg)](https://artichoke.github.io/artichoke/artichoke_vfs/)
[![mruby backend documentation](https://img.shields.io/badge/docs-artichoke--backend-blue.svg)](https://artichoke.github.io/artichoke/artichoke_backend/)
[![mruby-sys documentation](https://img.shields.io/badge/docs-mruby--sys-blue.svg)](https://artichoke.github.io/artichoke/mruby_sys/)

<p align="center">
  <img width="200" height="200" src="https://artichoke.github.io/artichoke/logo.svg">
</p>

Artichoke is a Ruby implementation written in Rust. Artichoke aspires to be
compatible with [Ruby 2.6.3](https://github.com/ruby/ruby/tree/v2_6_3).

## Why Artichoke?

Artichoke is a work-in-progress. When functional, Artichoke will improve upon
MRI in the following ways:

- ❌
  [True parallelism with no GIL](https://github.com/artichoke/artichoke/milestone/4).
- ❌
  [Optional multi-threading](https://github.com/artichoke/artichoke/milestone/4).
- ❌
  [Deterministic garbage collection](https://github.com/artichoke/artichoke/milestone/5).
- ✅ Single binary distribution (all Ruby sources from core and stdlib are
  embedded in `artichoke` executable).
- ❌
  [WebAssembly build target](https://github.com/artichoke/artichoke/milestone/6).
  Partially supported with the wasm32-unknown-emscripten target on the
  [playground](https://artichoke.github.io/artichoke/).
- ❌ [MRI](https://github.com/ruby/ruby)-compatible
  [C API](https://github.com/artichoke/artichoke/milestone/7).
- ❌ [mruby](https://github.com/mruby/mruby)-compatible
  [C API (all 311 `MRB_API` functions)](https://github.com/artichoke/artichoke/milestone/7).
- ❌
  [Emoji identifiers (classes, modules, methods, variables) 💪](https://github.com/artichoke/artichoke/milestone/8).
- ❌
  [Optional Standard Library](https://github.com/artichoke/artichoke/milestone/9).
- ✅
  [Native Rust extensions exposed via `require` of virtual files](https://github.com/artichoke/artichoke/milestone/10).
- ❌
  [Filesystem access is either via the system or via an in-memory virtual filesystem](https://github.com/artichoke/artichoke/milestone/11).

Artichoke will deviate from MRI in the following ways:

- The only supported encodings are UTF-8,
  [maybe UTF-8](https://github.com/BurntSushi/bstr), and binary.
- Ruby source files are always interpreted as UTF-8.

## ruby/spec

Artichoke intends to pass 100% of [ruby/spec](/spec-runner/spec/ruby) with the
exception of specs for non-UTF-8 encodings. To view current progress on
ruby/spec compliance, see
[`scripts/spec-compliance.sh`](/scripts/spec-compliance.sh) or the tracking
milestones for ❌
[language](https://github.com/artichoke/artichoke/milestone/1), ❌
[Core](https://github.com/artichoke/artichoke/milestone/2), and ❌
[Standard Library](https://github.com/artichoke/artichoke/milestone/3).

## Try Artichoke

You can [try Artichoke in your browser](https://artichoke.github.io/artichoke/).
The Artichoke Playground runs a [WebAssembly](https://webassembly.org/) build of
Artichoke.

If you would prefer to run a local build,
[set up a Rust toolchain](/CONTRIBUTING.md#rust-toolchain) and launch an
interactive Artichoke shell with:

```shell
cargo run -p artichoke-frontend --bin airb
```

## Contributing

Artichoke aspires to be a Ruby 2.6.3-compatible implementation of the Ruby
programming language.
[There is lots to do](https://github.com/artichoke/artichoke/issues).

If Artichoke does not run Ruby source code in the same way that MRI does, it is
a bug and we would appreciate if you
[filed an issue so we can fix it](https://github.com/artichoke/artichoke/issues/new).

If you would like to contribute code 👩‍💻👨‍💻, find an issue that looks interesting
and leave a comment that you're beginning to investigate. If there is no issue,
please file one before beginning to work on a PR.

### Discussion

If you'd like to engage in a discussion outside of GitHub, you can
[join Artichoke's public Discord server](https://discord.gg/QCe2tp2).
