---
title: /jobpanel edit
tags: [kuronekobot, guide]
icon: dot
oder: 95
---

# /jobpanel edit
## 使用方法
```
/jobpanel edit <option>

```
!!!info
このコマンドはオプションを指定しなくても使用可能ですが、指定していない場合効果がありません。
!!!

オプション名 | 概要 | 必要かどうか
--- | --- | --
color | 役職パネルの色 | いいえ
title | 役職パネルのタイトル | いいえ
attachmentoption | 役職パネルの添付画像を削除するかどうか | いいえ
image | 役職パネルに添付する画像 | いいえ

## 動作
```mermaid
graph LR
    A{/jobpanel edit}
    A -->|colorがある場合| B[役職パネルの色を指定された色に変更]
    A -->|titleがある場合| C[役職パネルのタイトルを指定されたタイトルに変更]
    A -->|attachmentoptionがある場合| D[役職パネルに添付されている画像を削除]
    A -->|imageがある場合| E[役職パネルに指定された画像を添付]
```