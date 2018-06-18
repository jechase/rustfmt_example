## Reproducing

`cargo +nightly fmt` will apply and `cargo +nightly fmt -- --check` will show the following diff:

```
Diff in /tmp/rust_demo/src/main.rs at line 1:
 use std::{
-    env,
-    fs,
+    env, fs,
     io::{
         self,
         BufRead,
```

Opening the project with vscode/rls, however, will keep `env` and `fs` on their own lines as configured.

## Versions

```
$ rustup show
...

active toolchain
----------------

nightly-x86_64-unknown-linux-gnu (default)
rustc 1.28.0-nightly (86a8f1a63 2018-06-17)

$ cargo +nightly fmt -- --version
rustfmt 0.8.2-nightly (08da30d 2018-06-06)
```