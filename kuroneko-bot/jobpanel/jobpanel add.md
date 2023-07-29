---
title: /jobpanel add
tags: [kuronekobot, guide]
icon: dot
order: 100
---

# /jobpanel add
## 使用方法
```
/jobpanel add role1: <option>
```

オプション名 | 概要 | 必要かどうか
--- | --- | --
role1 | 付与する役職 | **<u>はい</u>**
emoji1 | role1に対応させる絵文字 | いいえ
role2 ~ role10 | role1以外で付与する役職 | いいえ
emoji2 ~ emoji10 | role2 ~ role10に対応させる絵文字 | いいえ

## 動作
```mermaid
graph LR
    A{/jobpanel add role1:}
    A --> B[付与するロール及び付与する際に押す絵文字を追加]
    B -->|対応の絵文字を押す| C[ロール付与]
    B -->|role2以上かemoji2以上があった場合| D[他のロールを追加]
    B -->|emoji1があった場合| E[指定された絵文字をリアクション]
```