---
title: "Gmailで指定したEメールアドレス以外に自動通知を送る方法【不在通知｜Gメール】"
date: 2021-12-16
lastmod: 2021-12-16
# post thumb
images:
  - "images/blog/canned-response-negate.jpg"
# description
description: "Gmailで特定のEメールアドレス以外にだけ自動通知を送る方法について解説します。"
# Taxonomies
categories: ["IT"]
tags: ["IT"]
type: "regular" # available type (epic, trending, popular, or regular)
draft: false
share: true
---
こんにちは！めお(<u><a href="https://twitter.com/meeowmiya" target="_blank">@meeowmiya</a></u>)です。アメリカ在住8年目、フリーランスのイラストレーターをしています。


{{< say-left >}}
休暇で不在だけど、Aの案件だけは対応したい
{{< /say-left >}}

{{< say-left >}}
会社的には休みをとったことになっているけど、社内案件は対応しないといけない
{{< /say-left >}}

本記事では、こういった疑問にお答えし、<span class="keiko-red">**指定したEメールアドレス以外の自動通知を送る方法を紹介します。**</span>

特定のメールアドレスに自動通知を送信する方法も紹介しています。

基本的にはやり方は👆と同じで、フィルターの設定方法だけが違います。

必要な箇所まで読み飛ばしたい場合は<a href="">こちらをクリック</a>してください。

それでは詳しく見ていきましょう。

{{< toc >}}

## Gメールのデフォルト不在通知

Gメールのデフォルトの不在通知の設定では、<span class="keiko-red">**「連絡先に登録されているユーザーにのみ返信する」選択肢しかないため、より詳細な設定はできません。**</span>

![image](../../images/blog-content/canned-response-2.jpg)<br><br>


次に紹介する方法では、<span class="keiko-red">**指定した人以外にだけ自動通知を送る設定ができます！**</span>

## ①テンプレートの有効化

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

歯車から**すべての設定を表示**を選択


![image](../../images/blog-content/canned-response-1.jpg)<br><br>


<span class="keiko-red">**フィルタとブロック中のアドレス**</span>を選択し、<span class="keiko-red">**新しいフィルタを作成**</span>をクリック

![image](../../images/blog-content/canned-response-9.jpg)<br><br>

特定の人にだけフィルタを適応したい場合は、From欄に、自動通知したいEメールアドレスを入力しましたが、今回は指定の人を無効にします。

<指定したメールアドレス>でない場合のみ定型文を返信する、というロジックです。


<span class="keiko-red">**含まない**</span>欄に、自動通知を送りたくない人のメールアドレスを次のように入力し、<span class="keiko-red">**続行**</span>します。

* **from: <メールアドレス>**
![image](../../images/blog-content/canned-response-negate-10.jpg)<br><br>


複数人いる場合はORで区切ればオッケーです。この時、すべてのメールアドレスの前にfrom: をつける必要があるのでご注意ください。

例：from: taro\@example.com OR from: tanaka\@example.com

<span class="keiko-red">**テンプレートを送信**</span>をクリックし、ドロップダウンから先ほど作成した自動通知（○月○日〜○月○日 休暇通知）を選択し、<span class="keiko-red">**フィルタを作成**</span>


![image](../../images/blog-content/canned-response-negate-11.jpg)<br><br>


これで完了です！

## 自動通知設定の編集

### 自動通知を送信するEメールアドレスを変更する場合

<span class="keiko-red">**歯車**</span>から<span class="keiko-red">**すべての設定を表示**</span>を選択


![image](../../images/blog-content/canned-response-1.jpg)<br><br>


<span class="keiko-red">**フィルタとブロック中のアドレス**</span>で、編集したいフォルダの右側の**編集**をクリック


![image](../../images/blog-content/canned-response-negate-12.jpg)<br><br>


設定を変更し、<span class="keiko-red">**続行**</span>をクリック

![image](../../images/blog-content/canned-response-negate-13.jpg)<br><br>


<span class="keiko-red">**フィルタを更新**</span>をクリック

![image](../../images/blog-content/canned-response-negate-14.jpg)<br><br>


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


![image](../../images/blog-content/canned-response-negate-18.jpg)<br><br>


## 注意点 

特定のEメールアドレスからの設定と同様に、次のことに注意してください。

* 日時を設定できないので、<span class="keiko-red">**不要になった段階で必ずフィルタを削除する**</span>
* 送信先のメールアドレスが、**＜メールアドレス＞+canned.response\@gmail.com**に変更される。


## まとめ

以上「Gmailで指定したEメールアドレス以外に自動通知を送る方法」でした！

特定のEメールアドレスにだけ自動通知を送る方法も紹介していますので、合わせてご覧ください。


「役に立った」と思っていただけたら、シェアいただけますと幸いです。ブログやWEBサイトなどでのご紹介もとても嬉しいです!

