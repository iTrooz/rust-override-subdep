This repository shows you how to patch a transitive dependency (subdependency) in Rust.

The crate A uses crates B that uses the crate home. In this repository, I override B's dependency on home from A, to replace it by home-patch

Notes:
- you might need to run `cargo update` in your repository after adding the patch
- The override package (home-patch) here needs to have the version that `B` wants

Sources:
- https://doc.rust-lang.org/cargo/reference/overriding-dependencies.html#the-patch-section
- https://users.rust-lang.org/t/specifying-subdependencies-versions/67939/3
