---
title: /help
tags: [artifacter, guide]
icon: dot
order: 97
---

# /help
## 概要
コマンドの説明や自分のUIDの変更/削除等が行えます。

!!!
コマンドの説明などの掲載内容は[ArtifacterModifiedについて](about.md)と同様です。
!!!

## 使用方法
```
/help
```

## 動作
```mermaid
graph LR
    A{/help}
    A --> B[Artifacterについて]
    A --> C[uidの変更及び削除]
    C --> D[uid登録及び削除フォーム]
```