---
title: "Gmailで特定のEメールアドレスにだけ自動通知を送る方法【不在通知｜Gメール】"
date: 2021-12-14
lastmod: 2021-12-14
# post thumb
images:
  - "images/blog/canned-response.jpg"
# description
description: "Gmailで特定のEメールアドレスにだけ自動通知を送る方法について解説します。"
# Taxonomies
categories: ["IT"]
tags: ["ライフハック"]
type: "regular" # available type (epic, trending, popular, or regular)
draft: false
share: true
---
こんにちは！めお(<u><a href="https://twitter.com/meeowmiya" target="_blank">@meeowmiya</a></u>)です。アメリカ在住8年目、フリーランスのイラストレーターをしています。


{{< say-left >}}
A社の人にだけ不在通知を送りたい。でも、他の人には自動通知は送りたくない...
{{< /say-left >}}


{{< say-left >}}
社内の人にだけ不在通知を送りたい
{{< /say-left >}}

本記事では、こういった疑問にお答えし、<span class="keiko-red">**特定のEメールアドレスにだけ自動通知を送る方法を紹介します。**</span>

**指定したメールアドレス<span class="keiko-red">以外に**</span>自動通知を送信する方法も紹介していますので、設定しやすい方に合わせてご覧ください。

<div class="iframely-embed"><div class="iframely-responsive" style="padding-bottom: 52.25%; padding-top: 120px;"><a href="https://menglish.jp/post/canned-response-negate/" data-iframely-url="//cdn.iframe.ly/ej6DaGy"></a></div></div><script async src="//cdn.iframe.ly/embed.js" charset="utf-8"></script>

それでは詳しく見ていきましょう。

{{< toc >}}

## Gメールのデフォルト不在通知

よく使われるデフォルトの不在通知の設定は、次のように行います。

<span class="keiko-red">**歯車**</span>から<span class="keiko-red">**すべての設定を表示**</span>を選択


![image](../../images/blog-content/canned-response-1.jpg)<br><br>


<span class="keiko-red">**全般**</span>を選択し、スクロールすると不在通知が作成できます。

![image](../../images/blog-content/canned-response-2.jpg)<br><br>


しかし、<span class="keiko-red">**デフォルト設定では「連絡先に登録されているユーザーにのみ返信する」選択肢しかないため、より詳細な設定はできません。**</span>

次に紹介する方法では、<span class="keiko-red">**特定の人にだけ自動通知を送る設定ができます！**</span>

## ①テンプレートを有効にする

<span class="keiko-red">**歯車**</span>から<span class="keiko-red">**すべての設定を表示**</span>を選択

![image](../../images/blog-content/canned-response-1.jpg)<br><br>


<span class="keiko-red">**詳細**</span>を選択し、<span class="keiko-red">**テンプレート**を**有効にする**</span>を選択

![image](../../images/blog-content/canned-response-3.jpg)<br><br>


スクロールし、<span class="keiko-red">**変更を保存**</span>をクリック

![image](../../images/blog-content/canned-response-4.jpg)<br><br>


## ②自動通知を作成する

<span class="keiko-red">**＋作成**</span>でメール作成画面を開き、自動通知を下書きします。

![image](../../images/blog-content/canned-response-5.jpg)<br><br>


<span class="keiko-red">**︙**</span>をクリックします。

![image](../../images/blog-content/canned-response-6.jpg)<br><br>


<span class="keiko-red">**テンプレート**</span>から<span class="keiko-red">**下書きをテンプレートとして保存、新しいテンプレートとして保存**</span>を選択


![image](../../images/blog-content/canned-response-7.jpg)<br><br>


**※👆で「テンプレートを有効」にしていないと「テンプレート」は表示されないのでご注意ください。**

テンプレートに名前をつけ、<span class="keiko-red">**保存**</span>をクリック（ここでは「○月○日〜○月○日 休暇通知」と命名）

![image](../../images/blog-content/canned-response-8.jpg)<br><br>


## ③特定の人にだけ自動通知を送付する設定をする

<span class="keiko-red">**歯車**</span>から<span class="keiko-red">**すべての設定を表示**</span>を選択


![image](../../images/blog-content/canned-response-1.jpg)<br><br>


<span class="keiko-red">**フィルタとブロック中のアドレス**</span>を選択し、<span class="keiko-red">**新しいフィルタを作成**</span>をクリック

![image](../../images/blog-content/canned-response-9.jpg)<br><br>


From欄に、自動通知したいEメールアドレスを入力し、<span class="keiko-red">**フィルタを作成**</span>をクリック

![image](../../images/blog-content/canned-response-10.jpg)<br><br>


複数人いる場合はORで区切ればオッケーです。

例：taro\@example.com OR tanaka\@example.com

<span class="keiko-red">**テンプレートを送信**</span>をクリックし、ドロップダウンから先ほど作成した自動通知（○月○日〜○月○日 休暇通知）を選択し、<span class="keiko-red">**フィルタを作成**</span>


![image](../../images/blog-content/canned-response-11.jpg)<br><br>


これで完了です！

## 自動通知設定の編集

### 自動通知を送信するEメールアドレスを変更する場合

<span class="keiko-red">**歯車**</span>から<span class="keiko-red">**すべての設定を表示**</span>を選択


![image](../../images/blog-content/canned-response-1.jpg)<br><br>


<span class="keiko-red">**フィルタとブロック中のアドレス**</span>で、編集したいフォルダの右側の**編集**をクリック


![image](../../images/blog-content/canned-response-12.jpg)<br><br>


設定を変更し、<span class="keiko-red">**続行**</span>をクリック

![image](../../images/blog-content/canned-response-13.jpg)<br><br>


<span class="keiko-red">**フィルタを更新**</span>をクリック

![image](../../images/blog-content/canned-response-14.jpg)<br><br>


### 文面を変更する場合


<span class="keiko-red">**＋作成**</span>でメール作成画面を開き、<span class="keiko-red">**︙**</span>をクリックします。

![image](../../images/blog-content/canned-response-15.jpg)<br><br>


<span class="keiko-red">**テンプレート**</span>から先ほど保存したテンプレート（○月○日〜○月○日 休暇通知）を選択


![image](../../images/blog-content/canned-response-16.jpg)<br><br>


文面が挿入されるので、編集し、<span class="keiko-red">**︙**</span>をクリック

![image](../../images/blog-content/canned-response-6.jpg)<br><br>


<span class="keiko-red">**テンプレート**</span>から<span class="keiko-red">**下書きをテンプレートとして保存**、**先ほど保存したテンプレート（○月○日〜○月○日 休暇通知）を選択**</span>し、上書きします。


![image](../../images/blog-content/canned-response-17.jpg)<br><br>


## 自動通知設定の削除


<span class="keiko-red">**歯車**</span>から<span class="keiko-red">**すべての設定を表示**</span>を選択


![image](../../images/blog-content/canned-response-1.jpg)<br><br>


<span class="keiko-red">**フィルタとブロック中のアドレス**</span>で、編集したいフォルダの右側の<span class="keiko-red">**削除**</span>をクリック


![image](../../images/blog-content/canned-response-18.jpg)<br><br>


## 注意点 

### 日時設定

フィルタを使った設定では、日時を設定できないので、<span class="keiko-red">**不要になった段階で必ずフィルタを削除するよう**</span>ご注意ください（テンプレートは削除しない限り保存でき、次の機会に使用できます）。

### メールアドレス


この設定を使った自動送信の場合、送信先のEメールアドレスが**＜メールアドレス＞+canned.response\@gmail.com**に変更されます。

よっぽど注意しないと気づきませんが、自動送信を設定したという形跡が残るのでご注意ください。


## まとめ

以上「Gmailで特定のEメールアドレスに自動通知を送る方法」でした！

**指定したメールアドレス<span class="keiko-red">以外に**</span>自動通知を送信する方法も紹介していますので、合わせてご覧ください。

<div class="iframely-embed"><div class="iframely-responsive" style="padding-bottom: 52.25%; padding-top: 120px;"><a href="https://menglish.jp/post/canned-response-negate/" data-iframely-url="//cdn.iframe.ly/ej6DaGy"></a></div></div><script async src="//cdn.iframe.ly/embed.js" charset="utf-8"></script>


「役に立った」と思っていただけたら、シェアいただけますと幸いです。ブログやWEBサイトなどでのご紹介もとても嬉しいです!

