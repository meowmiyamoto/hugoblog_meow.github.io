---
title: "ブログ選びに迷っている方に「Hugo」がイチオシです！【アフィリエイト ｜プログラミング｜オウンドメディア】"
date: 2021-09-13
lastmod: 2021-09-13
# post thumb
images:
  - "images/blog/hugo-intro.jpg"
# description
description: "記事数2500以下の小規模ブログに「Hugo」がイチオシの理由を解説します。"
# Taxonomies
categories: ["メディア運用","ブログ","IT"]
tags: ["ブログ"]
type: "regular" # available type (epic, trending, popular, or regular)
draft: false
share: true
---
こんにちは！めお(<u><a href="https://twitter.com/meeowmiya" target="_blank">@meeowmiya</a></u>)です。


{{< say-left >}}
ブログを始めたいけど、Wordpressは使いにくいし、はてなブログやnoteは自由度が低い。かゆいところに手が届くサービスはないかな
{{< /say-left >}}

こういった疑問にお答えし、当ブログが使っているHugoというシステムについて紹介します。

この記事を読んで得られることは次の通りです。

* Hugoなどの静的サイトジェネレーターの仕組みがわかる
* 個人ブログ運営にHugoが最適な理由がわかる
* Hugoを使い始めるのに必要な知識と環境がわかる

私自身、ブログ界隈のメインストリームであるWordpressやレンタルブログでは満足できずにいました。

{{< notice "link" >}}
<div class="iframely-embed"><div class="iframely-responsive" style="height: 140px; padding-bottom: 0;"><a href="https://menglish.jp/post/wordpress-not-really/" data-iframely-url="//cdn.iframe.ly/t9Uuwja?card=small"></a></div></div><script async src="//cdn.iframe.ly/embed.js" charset="utf-8"></script><br><br>
<div class="iframely-embed"><div class="iframely-responsive" style="height: 140px; padding-bottom: 0;"><a href="https://menglish.jp/post/note-not-really/" data-iframely-url="//cdn.iframe.ly/906Ba69?card=small"></a></div></div><script async src="//cdn.iframe.ly/embed.js" charset="utf-8"></script>
{{< /notice >}}

Hugoは少し学習コストがありますが、<span class="keiko-red">**使いやすさ・自由度・セキュリティ・SEO・ページのサイズなど多くの面において他のブログサービスとは圧倒的に一線を画しています。**</span>

それでは詳しく見ていきましょう。

{{< toc >}}

## 静的サイトジェネレーターとは

Hugoは静的サイトジェネレーターというシステムを使ってサイトを構築します。

Wordpressなど、CMS（コンテンツ管理システム）を使ってページを生成するシステムでは、①ページにアクセスがあるごとに②データベースやテキストファイルからコンテンツを取得して③ウェブサイトを生成するという仕組みで作られています。
![image](../../images/blog-content/hugo-intro-1.jpg)<br><br>

一方で静的サイトジェネレーターはデータベースを使用せず、①プログラムを実行すると、③htmlやCSSなどのテキストファイルからWebサイトが生成され、③アクセスがあればページが表示されるという仕組みです。
![image](../../images/blog-content/hugo-intro-2.jpg)<br><br>


ふたつを見比べてみましょう。
![image](../../images/blog-content/hugo-intro-1.jpg)
![image](../../images/blog-content/hugo-intro-2.jpg)<br><br>

<span class="keiko-red">**Wordpressのページ表示工程が複雑なのに対し、静的サイトジェネレーターはシンプル**</span>です。

表示するデータが多い複雑なウェブサイトを作るときにはWordpressなどが向きますが、記事数2500以下の比較的シンプルなページを作るのであれば、Wordpressはオーバーキルです。

* Wordpressは、データが大きい複雑なウェブサイトに向いている
* 記事数2500以下のシンプルなブログでは静的サイトジェネレーターで十分

### 静的サイトジェネーターを使うメリット

![image](../../images/blog-content/hugo-intro-3.jpg)<br><br>

![image](../../images/blog-content/hugo-intro-4.jpg)<br><br>

<span class="keiko-red">**静的サイトジェネレーターはパソコンさえあればネットなしでページを生成できます。**</span>

テキストファイルを作り、ターミナルでHugoを実行するだけでウェブサイトを構築します。

ローカル環境（ネットなし）で生成できるため、<span class="keiko-red">**ページ生成が速く、セキュリティも強固で、バックアップも簡単に取れます。**</span>

一方で、Wordpressはネット環境に繋がないと編集や管理ができません。

すべてがネット依存のため、生成が遅く、セキュリティも脆弱で、わざわざファイルをダウンロードしなければバックアップがとれません。

### 静的サイトジェネレーターの種類

静的サイトジェネレーターにはJekyll, Hugo, Gatsby.jsなどの種類があり、それぞれRuby on Rails, Go、Reactなど使われる言語が異なります。

そして、それぞれの言語を学ぶ必要があります。

しかし今からブログを始めるのであれば、どうせ知識をつけないとガチ運営できないのはWordpressでも他のプラットフォームでも同じです。

そのため、<span class="keiko-red">**静的サイトジェネレーターを使うためのラーニングコストはWordpressを学ぶためのものと同等と考えてオッケーです。**</span>

当ブログは静的サイトジェネレーターの中でもGo言語を使ったHugoを使用してブログを運営しています。

## 個人ブログにHugoが最適な理由

記事数2500以下の個人ブログで、Hugoが最適な理由は次の通りです。

1. ページ生成速度
2. セキュリティ
3. 多言語対応
4. 値段
5. テーマや実装の簡単さ
6. 界隈のクリーンさ
7. SEO


### ①ページ生成速度

ページをロードするたびにリクエストを送ってページを生成する従来のブログと静的サイトジェネレーターが一線を画すのは、データベースを介さずにサイトを生成することにより表示速度が高速な点にあります。

特に<span class="keiko-red">**Googleが使用し「世界最速の表示速度」を誇るGo言語を使うHugoの表示速度は圧倒的です。**</span>

### ②セキュリティ

Hugoを始めとする静的サイトジェネレーターにはデータベースが存在しないため、<span class="keiko-red">**データベースを使う際にセキュリティが脆弱になるWordpressの問題がそもそも存在しません。**</span>

### ③多言語対応

Hugoはディレクトリやconfigファイルの構造上、<span class="keiko-red">**多言語対応が非常に簡単**</span>です。

イラストレーターやエンジニアなど世界で活躍するクリエイターにとって日英対応のサイトを使う重要性は右肩上がりという現状、多言語サイトを一括で管理できるのは大幅なコスト削減に繋がります。

### ④値段

Hugoは標準装備で高機能のため、有料プラグインがほとんど必要ありません。

<span class="keiko-red">**Hugoを使ってサイトを運営するコストは実質ゼロと言っていい**</span>でしょう。

### ⑤テーマや実装の簡単さ

静的サイトジェネレーターは難しいように見えますが、現在はかなり成熟してきています。

<span class="keiko-red">**過去には専門知識がないと難しかったことも、いまではかなり簡単になってきました。**</span>

テーマも充実しているため、ファイルを見ながら学習することも十分可能です。


### ⑥界隈のクリーンさ

Wordpressやレンタルブログがまだまだ主流なブログ界隈では、胡散臭い人が山ほどいます。

参入障壁がちょっとだけ高いが故に、<span class="keiko-red">**Hugoや他の静的サイトジェネレーター界隈は胡散臭いブロガーはあんまりいません。**</span>

何度かチャレンジしてWordpressもレンタルブログも個人的にはあまり良さを感じられませんでした。

そのため手放しで「Wordpress最高！」という人には少し身構えるようになりました。

ブログ運営の「できるだけ正直でいたい」というブランディング的にWordpressを意識的に外れたという経緯もあります。

### ⑦SEO

<span class="keiko-red">**最速の表示速度を誇り、セキュリティの脆弱性も低いHugo**</span>はWordpressには実現不可能な面においてSEOに大きくプラスです。

## Hugoを使い始めるのに必要な知識と環境


### テーマ

全くの初心者であれば<span class="keiko-red">**テーマを使って大枠を作ってしまうのが一番手っ取り早い**</span>です。

Hugo公式テーマは<a href ="https://themes.gohugo.io/" target ="_blank"><u>こちらのサイト</u></a>から入手できます。

また有料テーマは<a href ="https://themefisher.com/" target ="_blank"><u>こちらのサイト</u></a>が配信しています。

### 公式資料とテーマのファイルを見てプログラミングを学べる

Hugoの環境設定は<a href ="https://gohugo.io/getting-started/quick-start/" target ="_blank"><u>こちらのサイト</u></a>から詳しく見てみてください。

<span class="keiko-red">**簡単なPythonやC言語を習得した方ならGo言語はさほど難しくない**</span>と思います。

またhtmlファイルを見て何となくの構造をつかめる方は、フォーラムなどを見ながらセットアップ可能です。

### 英語

<span class="keiko-red">**公式資料やフォーラムのほとんどは英語**</span>のため「英語で読める」というスキルが必要です。

とは言っても時間や翻訳機能付きで読めれば良いため、さほどハードルは高くありません。

## まとめ

以上「ブログ選びに迷っている方に「Hugo」がイチオシです！」でした！

Hugoは難しいように見えますが、いまではかなり簡単になってきました。

Wordpressや無料レンタルブログでは実現できない良さがたくさん詰まっているので、簡単なプログラミングができるブロガーにはかなりオススメです。

ぜひ参考にしてみてください！

「役に立った」と思っていただけたら、シェアいただけますと幸いです。ブログやWEBサイトなどでのご紹介もとても嬉しいです!