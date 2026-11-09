# rust-pkg

一组自建的 Rust 公共 crate 集合（workspace）。

## 引用
可用 `branch` / `tag` / `rev` 指定版本，不写则默认 `main`。

```toml
[dependencies]
file-utils = { git = "https://github.com/MakoStar/rust-pkg", branch = "main"}
```

## 本地
改 crate 时不用先 push，在消费项目里用 `[patch]` 指向本地路径, 改完删掉这段即可:

```toml
[patch."https://github.com/MakoStar/rust-pkg"]
file-utils = { path = "../rust-pkg/crates/file-utils" }
```

## 测试

```bash
cargo build --all
cargo test --all
```
