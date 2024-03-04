---
title: 原神API
icon: dot
---

# 原神API
## 概要
Enka.NetworkのAPI情報を整理したAPIものを返すAPIとなっております。

GETリクエストでAPIにアクセスし、原神のユーザーの原神のキャラクター情報をjson形式で返すAPIとなっています。

API仕様
```
https://genshin-api.kuroneko6423.com/api/genshindata/?uid=UID&scoretype=ATTACK、HP、CHARGE、ELEMENT、DEFENCEのどれか&charaName=キャラクター名
```
当てはめる値 | 概要 |
-- | -- |
UID | 原神のUID | 
ATTACK | 
HP | 
CHARGE | 
ELEMENT | 
DEFENCE | 防御力のスコア

リクエスト例
```
https://genshin-api.kuroneko6423.com/api/genshindata/?uid=830322314&scoretype=ATTACK&charaName=ディオナ
```
結果例
```
{"uid":830322314,"Character":{"Name":"ディオナ","Const":0,"Level":50,"Love":1,"Status":{"HP":8999,"攻撃力":296,"防御力":390,"元素熟知":97,"会心率":5,"会心ダメージ":50,"元素チャージ効率":105.8,"氷元素ダメージ":6},"Talent":{"通常":1,"スキル":1,"爆発":1},"Base":{"HP":5074,"攻撃力":222,"防御力":318}},"Weapon":{"name":"絶弦","Level":20,"totu":1,"rarelity":4,"BaseATK":109,"Sub":{"name":"元素熟知","value":64}},"Score":{"State":"攻撃","total":0,"flower":0,"wing":0,"clock":0,"cup":0,"crown":0},"Artifacts":{"flower":{"type":"冒険者","Level":5,"rarelity":3,"main":{"option":"HP","value":1040},"sub":[{"option":"元素チャージ効率パーセンテージ","value":3.1},{"option":"元素熟知","value":10}]},"wing":{"type":"冒険者","Level":5,"rarelity":3,"main":{"option":"攻撃力","value":68},"sub":[{"option":"元素チャージ効率パーセンテージ","value":2.7},{"option":"HP","value":115}]},"clock":{"type":"冒険者","Level":5,"rarelity":3,"main":{"option":"防御パーセンテージ","value":16},"sub":[{"option":"元素熟知","value":14},{"option":"HP","value":143}]},"cup":{"type":"医者","Level":9,"rarelity":3,"main":{"option":"HPパーセンテージ","value":19},"sub":[{"option":"HP","value":115},{"option":"防御力","value":11},{"option":"攻撃力","value":7}]},"crown":{"type":"冒険者","Level":4,"rarelity":3,"main":{"option":"HPパーセンテージ","value":11},"sub":[{"option":"元素熟知","value":10},{"option":"防御力","value":10}]}},"元素":"氷"}
```

サービスページ: https://genshin-api.kuroneko6423.com


:::danger warning
10秒間に100回以上リクエストをすると429が返されます。

APIのレートリミットの緩和を行いたい場合は[お問い合わせ](https://discord.com/invite/Y6w5Jv3EAR)をお願いします。

※APIの制限は提供しているAPIサービスと制限は共有されています。
:::