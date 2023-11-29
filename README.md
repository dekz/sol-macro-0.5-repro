```
sol-macro-repro λ cargo build
    Blocking waiting for file lock on package cache
    Updating crates.io index
    Blocking waiting for file lock on package cache
    Blocking waiting for file lock on package cache
   Compiling proc-macro2 v1.0.70
   Compiling unicode-ident v1.0.12
   Compiling serde v1.0.193
   Compiling syn v1.0.109
   Compiling version_check v0.9.4
   Compiling crunchy v0.2.2
   Compiling tiny-keccak v2.0.2
   Compiling cfg-if v1.0.0
   Compiling paste v1.0.14
   Compiling convert_case v0.4.0
   Compiling ruint-macro v1.1.0
   Compiling proc-macro-error-attr v1.0.4
   Compiling itoa v1.0.9
   Compiling proc-macro-error v1.0.4
   Compiling winnow v0.5.19
   Compiling hex-literal v0.4.1
   Compiling serde_json v1.0.108
   Compiling ryu v1.0.15
   Compiling quote v1.0.33
   Compiling equivalent v1.0.1
   Compiling hashbrown v0.14.3
   Compiling dunce v1.0.4
   Compiling syn v2.0.39
   Compiling heck v0.4.1
   Compiling indexmap v2.1.0
   Compiling alloy-sol-type-parser v0.5.0
   Compiling syn-solidity v0.5.0
   Compiling serde_derive v1.0.193
   Compiling derive_more v0.99.17
   Compiling ruint v1.11.1
   Compiling bytes v1.5.0
   Compiling const-hex v1.10.0
   Compiling alloy-primitives v0.5.0
   Compiling alloy-json-abi v0.5.0
   Compiling alloy-sol-macro v0.5.0
error[E0446]: private type `ExpCtxt<'_>` in public interface
  --> /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/to_abi.rs:10:1
   |
10 | / pub fn generate<T>(t: &T, cx: &ExpCtxt<'_>) -> TokenStream
11 | | where
12 | |     T: ToAbi,
13 | |     T::DynAbi: Verbatim,
   | |________________________^ can't leak private type
   |
  ::: /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/mod.rs:49:1
   |
49 |   struct ExpCtxt<'ast> {
   |   -------------------- `ExpCtxt<'_>` declared as private

error[E0446]: private type `ExpCtxt<'_>` in public interface
  --> /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/to_abi.rs:21:5
   |
21 |     fn to_dyn_abi(&self, cx: &ExpCtxt<'_>) -> Self::DynAbi;
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ can't leak private type
   |
  ::: /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/mod.rs:49:1
   |
49 | struct ExpCtxt<'ast> {
   | -------------------- `ExpCtxt<'_>` declared as private

error[E0446]: private type `ExpCtxt<'_>` in public interface
  --> /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/to_abi.rs:27:5
   |
27 |     fn to_dyn_abi(&self, cx: &ExpCtxt<'_>) -> Self::DynAbi {
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ can't leak private type
   |
  ::: /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/mod.rs:49:1
   |
49 | struct ExpCtxt<'ast> {
   | -------------------- `ExpCtxt<'_>` declared as private

error[E0446]: private type `ExpCtxt<'_>` in public interface
  --> /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/to_abi.rs:40:5
   |
40 |     fn to_dyn_abi(&self, cx: &ExpCtxt<'_>) -> Self::DynAbi {
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ can't leak private type
   |
  ::: /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/mod.rs:49:1
   |
49 | struct ExpCtxt<'ast> {
   | -------------------- `ExpCtxt<'_>` declared as private

error[E0446]: private type `ExpCtxt<'_>` in public interface
  --> /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/to_abi.rs:48:5
   |
48 |     fn to_dyn_abi(&self, cx: &ExpCtxt<'_>) -> Self::DynAbi {
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ can't leak private type
   |
  ::: /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/mod.rs:49:1
   |
49 | struct ExpCtxt<'ast> {
   | -------------------- `ExpCtxt<'_>` declared as private

error[E0446]: private type `ExpCtxt<'_>` in public interface
  --> /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/to_abi.rs:60:5
   |
60 |     fn to_dyn_abi(&self, cx: &ExpCtxt<'_>) -> Self::DynAbi {
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ can't leak private type
   |
  ::: /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/mod.rs:49:1
   |
49 | struct ExpCtxt<'ast> {
   | -------------------- `ExpCtxt<'_>` declared as private

error[E0446]: private type `ExpCtxt<'_>` in public interface
  --> /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/to_abi.rs:68:5
   |
68 |     fn to_dyn_abi(&self, cx: &ExpCtxt<'_>) -> Self::DynAbi {
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ can't leak private type
   |
  ::: /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/mod.rs:49:1
   |
49 | struct ExpCtxt<'ast> {
   | -------------------- `ExpCtxt<'_>` declared as private

error[E0446]: private type `ExpCtxt<'_>` in public interface
  --> /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/to_abi.rs:76:5
   |
76 |     fn to_dyn_abi(&self, cx: &ExpCtxt<'_>) -> Self::DynAbi {
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ can't leak private type
   |
  ::: /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/mod.rs:49:1
   |
49 | struct ExpCtxt<'ast> {
   | -------------------- `ExpCtxt<'_>` declared as private

error[E0446]: private type `ExpCtxt<'_>` in public interface
  --> /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/to_abi.rs:86:5
   |
86 |     fn to_dyn_abi(&self, _cx: &ExpCtxt<'_>) -> Self::DynAbi {
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ can't leak private type
   |
  ::: /Users/jacob/.cargo/registry/src/index.crates.io-6f17d22bba15001f/alloy-sol-macro-0.5.0/src/expand/mod.rs:49:1
   |
49 | struct ExpCtxt<'ast> {
   | -------------------- `ExpCtxt<'_>` declared as private

For more information about this error, try `rustc --explain E0446`.
error: could not compile `alloy-sol-macro` (lib) due to 9 previous errors
```
