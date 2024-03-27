---
title: 原神ビルドカードAPI
---

# 原神ビルドカードAPI
## 概要
Enka.NetworkのAPI情報を使用し、Artifacterのデザインを使用した画像生成APIとなっております。

GETリクエストでAPIにアクセスし、原神のユーザーの原神のキャラクター情報をjson形式で返し、原神のビルドカードを生成できるAPIとなっています。

---

# API仕様
## キャラクターリスト取得
```
https://genshin-image-gen-api.kuroneko6423.com/api/genshindata/?uid=UID
```
当てはめる値 | 概要 |
-- | -- |
UID | 原神のUID | 

リクエスト例
```
https://genshin-image-gen-api.kuroneko6423.com/api/genshindata/?uid=830322314
```
結果例
```
{"旅人":62,"ナヒーダ":60,"ベネット":60,"香菱":50,"ディオナ":50,"バーバラ":58,"早柚":20,"アンバー":40}
```

---

## ビルドカード生成
```
https://genshin-image-gen-api.kuroneko6423.com/api/generation/?uid=UID&scoretype=スコア&charaName=キャラクター名
```
当てはめる値 | 概要 |
-- | -- |
UID | 原神のUID | 
ATTACK | 攻撃力
HP | 体力
CHARGE | 元素チャージ
ELEMENT | 元素熟知
DEFENCE | 防御力のスコア
CHARACTER | 日本語の原神のキャラクター名(例: 旅人)

リクエスト例
```
https://genshin-image-gen-api.kuroneko6423.com/api/generation/?uid=830322314&scoretype=ATTACK&charaName=ディオナ
```
結果例
![image](/img/genshin-api/image-gen-api.png)

サービスページ: https://genshin-api.kuroneko6423.com


:::danger warning
10秒間に100回以上リクエストをすると「429 Too many Requests」が返されます。
<br></br>APIのレートリミットの緩和を行いたい場合は[お問い合わせ](https://discord.com/invite/Y6w5Jv3EAR)をお願いします。
<br></br>※APIの制限は提供しているAPIサービスと制限は共有されています。
:::
