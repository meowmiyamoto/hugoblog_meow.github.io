---
title: "Googleアドセンス「サイトの停止・利用不可」は「サイトマップ」と「robots.txt」で解決しよう【ブログ｜アフィリエイト 】"
date: 2021-09-05
lastmod: 2021-09-05
# post thumb
images:
  - "images/blog/adsene-site-unavailable.jpg"
# description
description: "Googleアドセンス「サイトの停止・利用不可」の解決方法を解説します。"
# Taxonomies
categories: ["ブログ","メディア運用"]
tags: ["ブログ"]
type: "regular" # available type (epic, trending, popular, or regular)
draft: false
share: true
---

こんにちは！めお(<u><a href="https://twitter.com/meeowmiya" target="_blank">@meeowmiya</a></u>)です。本記事ではアドセンス合格に一番てこずった「サイトの停止・利用不可」の解決方法について解説します。

{{< say-left >}}
サイトは見れるのに、「サイトの停止・利用不可」が出てアドセンスに合格できない。どうすればいい？
{{< /say-left >}}

という方はぜひ参考にして頂ければと思います。

<span class="keiko-red">**robots.txtとサイトマップを揃えれば多くの場合、この問題は解決します。**</span>ブログ自体とは全く関係のないテクニカル部分ですが、SEO強化にもつながるので一度確認しておいて損のない内容だと思います。

それでは詳しく見ていきましょう。

{{< toc >}}

## 「サイトの停止・利用不可」とは

![image](../../images/blog-content/adsense-site-unavailable-0.jpg)<br><br>
「サイトの停止・利用不可」になった場合、👆のようなエラーが出ます。

## 解決方法

<span class="keiko-red">**robots.txtとサイトマップを揃えれば多くの場合、この問題は解決します。**</span>

## ①robots.txtを設定する

### robots.txtとは

robots.txtとはGoogleやTwitterなどの検索エンジンに対して、サイトのどの部分にアクセスしてよいかを表記したものです。デフォルトの場合、Googleがブログにアクセスできていない可能性があり、そのために「サイト使用不可」のエラーが出ます。

### robots.txtの設定

解決策としては簡単で、robots.txtを通じてGoogleにブログへのアクセスを許可します。まずrootディレクトリにrobots.txtを作り、以下をコピペします。

```javascript
User-agent: *
Disallow: /

User-agent: Mediapartners-Google* 
Allow: /

User-agent: Googlebot-Mobile
Allow: /

User-agent: Adsbot-Google
Allow: /

User-agent: Googlebot
Allow: /

Sitemap: https://サイトURL/sitemap.xml
```



簡単に説明すると、まず最初の2行で、すべての検索エンジン(User-agent: U+002A)にサイト全体のアクセスをブロック(Disallow: /)します。3-14行目は様々なGoogle検索エンジン(Mediapartners-google U+002A, Googlebot-mobile, Adsbot-Google, Googlebot)にサイト全体のアクセスを許可(Allow: /)しています。サイトマップについては次項で解説します。

## ②サイトマップを設定する

### サイトマップとは

サイトマップとは、サイトのページ構成を一覧で記載したテキストファイルで、検索エンジンにサイト内容をわかりやすく伝えます。SEO強化に重要なサイトマップはアドセンスにも大きな役割を担っています。


### Googleサーチコンソールに登録する

サイトマップの登録にはGoogle サーチコンソールを使用します。アカウントを作成後、左上のメニューから「プロパティを追加」をクリックします。

![image](../../images/blog-content/adsense-site-unavailable-1.jpg)<br><br>


「プロパティタイプの選択」で「ドメイン」からURLを記入し「続行」をクリックします。

![image](../../images/blog-content/adsense-site-unavailable-2.jpg)<br><br>


「DNSレコードでの所有権の確認」では各ドメインサーバーにログインし、TXTレコードを登録します。

![image](../../images/blog-content/adsense-site-unavailable-3.jpg)<br><br>


ページを更新すると「所有権の確認」ができます。これでドメインの登録は完了です。

![image](../../images/blog-content/adsense-site-unavailable-4.jpg)<br><br>


### サイトマップを生成する

各ブログサービスを通じて、ますsitemap.xmlを用意してください。

左のメニューから「サイトマップ」を選択します。

![image](../../images/blog-content/adsense-site-unavailable-5.jpg)<br><br>


「新しいサイトマップの追加」からsitemap.xmlと入力してサイトマップを登録します。

![image](../../images/blog-content/adsense-site-unavailable-6.jpg)<br><br>


問題がなければ「成功しました」と出ます。これで登録は完了です。

![image](../../images/blog-content/adsense-site-unavailable-7.jpg)<br><br>


## まとめ

以上の2点を追加して再度アドセンスに挑戦してみてください。テクニカルな部分ですが、これを改善するだけで合格する確率はぐっと上がりますよ。ぜひチャレンジしてみてください！