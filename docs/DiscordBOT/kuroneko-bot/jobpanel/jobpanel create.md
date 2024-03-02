---
title: /jobpanel create
tags: [kuronekobot, guide]
icon: dot
order: 97
---

# create
## 使用方法
```
/jobpanel create role: <option>
```

オプション名 | 概要 | 必要かどうか
--- | --- | --
role | 付与する役職 | **<u>はい</u>**
emoji | roleに対応させる絵文字 | いいえ
color | 役職パネルの色 | いいえ
title | 役職パネルのタイトル | いいえ
image | 役職パネルに添付する画像 | いいえ

## 動作
```mermaid
graph LR
    A{/jobpanel create role:}
    A --> B[役職パネルを作成]
    B -->|emojiがある場合| C[emojiで指定されたリアクションを付与]
    B -->|colorがある場合| D[役職パネルの色を指定された色に変更]
    B -->|titleがある場合| E[役職パネルのタイトルを指定されたタイトルに変更]
    B -->|imageがある場合| F[役職パネルに指定された画像を添付]
```