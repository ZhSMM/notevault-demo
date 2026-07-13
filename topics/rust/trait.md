---
title: Rust trait
type: concept
tags: [rust, programming, trait, oop]
difficulty: 3
---

# Rust trait

Trait 定义了**类型可以做什么**（共享行为）。类似其他语言的 interface，但更强大。

## 定义

```rust
trait Summary {
    fn summarize(&self) -> String;
    
    fn default_summarize(&self) -> String {  // 默认实现
        String::from("(更多内容...)")
    }
}
```

## 实现

```rust
struct NewsArticle { headline: String, content: String }

impl Summary for NewsArticle {
    fn summarize(&self) -> String {
        format!("{}", self.headline)
    }
}
```

## 用作参数

```rust
fn notify(item: &impl Summary) {
    println!("新闻！{}", item.summarize());
}
```

## 关联概念

- [[Rust 所有权]]：trait 方法通常用引用接收
