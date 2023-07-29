---
title: /jobpanel
icon: gear
tags: [kuronekobot, guide]
order: 99
---

# /jobpanel
## 概要
役職を付与したり外したりするパネルに関するコマンドです。

## 使用方法
```
/jobpanel <subcommand>
```

!!!warning
このコマンドは単体では使用できません。サブコマンドの指定を行ってください。
!!!

!!!danger
サブコマンドの一部では **<u>役職パネルを選択していないと失敗します。</u>**  
[こちら](#役職パネルの選択方法)から役職パネルを選択してください。
!!!

サブコマンド名 | 概要 | ガイド
-- | -- | --
add | パネルに役職を追加します | [!badge variant="success" icon="paper-airplane" iconAlign="right" text="見る"](#add)
autoremove | 選択しているパネルに含まれる削除されたロールを取り除きます。 | [!badge variant="success" icon="paper-airplane" iconAlign="right" text="見る"](#autoremove)
copy | 選択しているパネルをコピーします。 | [!badge variant="success" icon="paper-airplane" iconAlign="right" text="見る"](#copy)
create | 役職パネルを作成します。 | [!badge variant="success" icon="paper-airplane" iconAlign="right" text="見る"](#create)
delete | 選択したパネルを削除します。 | [!badge variant="success" icon="paper-airplane" iconAlign="right" text="見る"](#delete)
edit | 選択したパネルのタイトルやカラーを変更します。 | [!badge variant="success" icon="paper-airplane" iconAlign="right" text="見る"](#edit)
refresh | 選択したパネルのリアクションをつけ直します。 | [!badge variant="success" icon="paper-airplane" iconAlign="right" text="見る"](#refresh)
remove | パネルから役職を削除します。 | [!badge variant="success" icon="paper-airplane" iconAlign="right" text="見る"](#remove)
selected | 現在選択しているパネルのリンクを返します。 | [!badge variant="success" icon="paper-airplane" iconAlign="right" text="見る"](#selected)

### add
#### 使用方法
```
/jobpanel add role1: <option>
```

オプション名 | 概要 | 必要かどうか
--- | --- | --
role1 | 付与する役職 | **<u>はい</u>**
emoji1 | role1に対応させる絵文字 | いいえ
role2 ~ role10 | role1以外で付与する役職 | いいえ
emoji2 ~ emoji10 | role2 ~ role10に対応させる絵文字 | いいえ

#### 動作
```mermaid
graph LR
    A{/jobpanel add role1:}
    A --> B[付与するロール及び付与する際に押す絵文字を追加]
    B -->|対応の絵文字を押す| C[ロール付与]
    B -->|role2以上かemoji2以上があった場合| D[他のロールを追加]
    B -->|emoji1があった場合| E[指定された絵文字をリアクション]
```

### autoremove
#### 使用方法
```
/jobpanel autoremove
```

#### 動作
```mermaid
graph LR
    A{/jobpanel autoremove}
    A --> B[選択されている役職パネルにリアクションされている不要な絵文字を削除]
```

### copy
#### 使用方法
```
/jobpanel copy
```

#### 動作
```mermaid
graph LR
    A{/jobpanel copy}
    A --> B[選択されている役職パネルを使用したチャンネルにコピー]
```

### create
#### 使用方法
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

#### 動作
```mermaid
graph LR
    A{/jobpanel create role:}
    A --> B[役職パネルを作成]
    B -->|emojiがある場合| C[emojiで指定されたリアクションを付与]
    B -->|colorがある場合| D[役職パネルの色を指定された色に変更]
    B -->|titleがある場合| E[役職パネルのタイトルを指定されたタイトルに変更]
    B -->|imageがある場合| F[役職パネルに指定された画像を添付]
```

### delete
#### 使用方法
```
/jobpanel delete
```

#### 動作
```mermaid
graph LR
   A{/jobpanel delete}
   A --> B[指定された役職パネルを削除]
```

### edit
#### 使用方法
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

#### 動作
```mermaid
graph LR
    A{/jobpanel edit}
    A -->|colorがある場合| B[役職パネルの色を指定された色に変更]
    A -->|titleがある場合| C[役職パネルのタイトルを指定されたタイトルに変更]
    A -->|attachmentoptionがある場合| D[役職パネルに添付されている画像を削除]
    A -->|imageがある場合| E[役職パネルに指定された画像を添付]
```

### refresh
#### 使用方法
```
/jobpanel refresh 
```

#### 動作
```mermaid
graph LR
   A{/jobpanel refresh}
   A --> B[絵文字をすべて削除し再度付与]
```

### remove
#### 使用方法
```
/jobpanel remove role1: <option> 
```

オプション名 | 概要 | 必要かどうか
-- | -- | --
role1 | 削除するロール | **<u>はい</u>**
role2 ~ role25 | role1以外に削除するロール | いいえ

#### 動作
```mermaid
graph LR
   A{/jobpanel remove role1:}
   A --> B[指定されたロールを役職パネルから削除]
   B -->|role2以上があった場合| C[指定されたロールも役職パネルから削除]
```

### selected
#### 使用方法
```
/jobpanel selected
```

#### 動作
```mermaid
graph LR
   A{/jobpanel refresh}
   A --> B[選択されている役職パネルのURLを表示]
```

## 役職パネルの選択方法
#### 役職パネルを右クリック
![](/static/jobpanel/1.webp)
#### アプリの「パネルを選択」をクリック
![](/static/jobpanel/2.webp)
#### 以下のようなメッセージが表示されればOK
![](/static/jobpanel/3.webp)

!!!warning
画像未準備
!!!