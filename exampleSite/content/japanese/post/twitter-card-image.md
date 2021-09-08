---
title: "Twitterカードが正しく表示されない問題の解決法まとめ【ブログ｜ツイッター｜SNS運用】"
date: 2021-09-06
lastmod: 2021-09-06
# post thumb
images:
  - "images/blog/twitter-card-image.jpg"
# description
description: "Twitterカードが正しく表示されない問題の解決方法をまとめています。"
# Taxonomies
categories: ["ブログ","メディア運用", "SNS運用", "IT"]
tags: ["IT"]
type: "regular" # available type (epic, trending, popular, or regular)
draft: false
share: true
---

こんにちは！めお(<u><a href="https://twitter.com/meeowmiya" target="_blank">@meeowmiya</a></u>)です。最近ようやくTwitterカードを画像付きで正しく表示できるようになりました。

![image](../../images/blog-content/twitter-card-image-1.jpg)<br><br>

{{< say-left >}}
私のページはツイッターでは画像がうまく表示されない。どうやったら直せる？
{{< /say-left >}}

という方に参考にして頂ければと思います。本記事では、👇のように表示されるツイートが画像と一緒に表示されるように修正する方法について解説します。

![image](../../images/blog-content/twitter-card-image-2.jpg)<br><br>


それでは詳しく見ていきましょう。

{{< toc >}}

## Twitterカード表示確認に使えるウェブサイト

Twitterカードの表示を確認するためには<a href="https://cards-dev.twitter.com/validator" target="_blank"><u>Twitter Card Validator</u></a>を使います。Card URLに表示確認をしたいアドレスを入れると、どのように表示されるか確認できます。

{{< notice "link2" >}}
<a href="https://cards-dev.twitter.com/validator" target="_blank"><u>Card Validator | Twitter Developer</u></a><br>
URLを入れると、Twitterタイムラインでどのように表示されるかプレビューできます。
{{< /notice >}}

便利なように見えますが、<span class="keiko-red">**詳細なエラーが出ないため自力でデバッグするしかない**</span>仕様になっています。以下、Twitterカードが正しく表示されない時の対処法一覧です。

## ①open graphとtwitter cardのメタタグを設定する

TwitterやFacebookをはじめとするSNSは、メタタグを読み込んでサムネカードを表示します。Facebookをはじめとするほとんどのサムネカードの表示は基本的にog (open graph)タグを使えばオッケーですが、Twitterだけは特別に独自仕様の設定が必要です。

まず各記事の<head></head>内に以下のメタタグを設定します。
```html
<meta property="og:title" content="記事タイトル">
<meta property="og:description" content="ページ概要 ">
<meta property="og:type" content="article"></meta>
<meta property="og:url" content="ページURL"></meta>
<meta property="og:image" content="サムネ画像"></meta>
<meta name="twitter:card" content=カードの種類"></meta>
<meta property="twitter:title" content="記事タイトル"></meta>
<meta property="twitter:description" content="ページ概要 "></meta>
<meta property="twitter:image" content="サムネ画像"></meta>
```
<br><br>
<span class="keiko-red">**twitterを正しく表示させるためにはtwitter:titleとtwitter:cardが必須**</span>です。カードタイプは、“summary”、“summary_large_image”、“app”、“player”のどれかが入力できますが、ブログの場合、“summary”か“summary_large_image”のどちらかを選びましょう。それぞれの違いは次の通りです。


summary_large_image👇

![image](../../images/blog-content/twitter-card-image-1.jpg)<br><br>


summary👇

![image](../../images/blog-content/twitter-card-image-3.jpg)<br><br>


## ②Twitterに画像ディレクトリのアクセスを許可する

robots.txtとはGoogleやTwitterなどの検索エンジンに対して、サイトのどの部分にアクセスしてよいかを表記したものです。デフォルトの場合、<span class="keiko-red">**Twitterが画像にアクセスできていない可能性があり、そのためにのエラーが出ます。**</span>

rootディレクトリにrobots.txtという名前のtxtファイルを作成し、以下を入力してください。

```javascript
User-agent: *
Disallow: /

User-agent: Twitterbot
Allow: /
```
まず最初の2行で、すべての検索エンジン(User-agent: \*\)にサイト全体のアクセスをブロック(Disallow: /)します。4-5行目ではTwitter検索エンジンにサイト全体のアクセスを許可(Allow: /)しています。既にrobots.txtがある方は、その他の設定に合わせてTwitterbotにアクセス許可を与えてください。


## ③画像リンクを絶対URLに

絶対URLとはリンク先をhttp://～まで含み全てそのまま記述する記載方法です。twitter:imageやog:imageのリンクがこの表記になっているか確認しましょう。<span class="keiko-red">**Twitterは絶対URLしか認識できません。**</span>


## ④画像サイズを確認する

Twitterは読み込める画像に制限があります。twitter:imageやog:imageで設定した画像が要件を満たしているか確認しましょう。ぶっちゃけほとんどの場合、画像が問題になることはないと思いますが、念のため。

* 144px x 144 px 以上
* 4096px x 4096 px 以下
* 5MB以下

## ⑤Twitter設定を確認する

<span class="keiko-red">**Twitter側の設定が間違っている場合も、Twitterカードはうまく表示されません。**</span>まずTwitterにログインし、「もっと見る」を選択し、「設定とプライバシー」を選択
![image](../../images/blog-content/twitter-card-image-4.jpg)<br><br>


「プライバシーとセキュリティ」から「ツイート」を選択

![image](../../images/blog-content/twitter-card-image-5.jpg)<br><br>


<span class="keiko-red">**「ツイートする画像/動画を不適切な内容を含むものとして設定する」にチェックマークが入っていない**</span>ことを確認します。

![image](../../images/blog-content/twitter-card-image-6.jpg)<br><br>


## ⑥CDN設定を確認する

<span class="keiko-red">**Twitter画像をCDNから配信しているとうまく画像が表示されません。**</span>わかりやすい場合は、twitter:imageやog:imageのURLがhttps://cdn.〜と始まっていることが確認できます。CDNを経由せずに配信する詳しい方法は、使用しているサービスのヘルプをご覧ください。

## ⑦ページによって画像が表示されたりされなかったりする場合

私の場合はこれでも解決せず、rootディレクトリに直に入っているindex.htmlでは画像が表示されるのに、サブディレクトリに入っている/post/example-post.htmlなどの記事では表示されないという謎仕様でした。解決策としては<span class="keiko-red">**twitter:imageタグを外し、og:imageだけ残してみてください。**</span>なぜかわかりませんが、私はこれで解決しました。<span class="keiko-red">**ツイッターはtwitter:cardとtwitter:titleさえあれば他のogタグも読めるみたいです。**</span>

## まとめ

以上「Twitterカードが正しく表示されない問題の解決法まとめ」でした！Twitter Validatorはデバッグできないのでしらみ潰しに試すしかありませんが、こちらの記事が少しでも参考になればと思います。より詳しく見てみたいという方は、以下のtwitter developer公式サイトを参考にしてください。

{{< notice "link" >}}
<div class="iframely-embed"><div class="iframely-responsive" style="height: 140px; padding-bottom: 0;"><a href="https://developer.twitter.com/en/docs/twitter-for-websites/cards/guides/troubleshooting-cards" data-iframely-url="//cdn.iframe.ly/JWqXDXh?card=small"></a></div></div><script async src="//cdn.iframe.ly/embed.js" charset="utf-8"></script>
{{< /notice >}}