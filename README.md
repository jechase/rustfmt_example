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