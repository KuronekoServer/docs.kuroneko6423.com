---
title: /bot report
icon: dot
tags: [kuronekobot, guide]
order: 100
---

# /bot report
## 概要
バグや要望を運営に送信します。

## 使用方法
```
/bot report
```

## 動作
```mermaid
graph LR
    A{/bot report}
    A --> B[レポート用フォームを表示]
    B -->|タイトル及び報告内容を記入| C[運営へ送信]
```