---
title: OpenJTalkAPI
icon: dot
---

# OpenJTalkAPI
## 概要
OpenJTalkを利用した音声合成APIです。

話者情報取得(GETリクエスト): `https://openjtalk-api.kuroneko6423.com/speakers`

音声合成(POST): `https://openjtalk-api.kuroneko6423.com/synthesize?text=読み上げる文字&type=話者&speed=0.7&pitch=0.7`

サービスページ: https://openjtalk-api.kuroneko6423.com

:::danger warning
10秒間に100回以上リクエストをすると429が返されます。

APIのレートリミットの緩和を行いたい場合は[お問い合わせ](https://discord.com/invite/Y6w5Jv3EAR)をお願いします。

※APIの制限は提供しているAPIサービスと制限は共有されています。
:::