# Zotero

Zoteroリファレンス自動生成します。

Zoteroから出力（Export）できるファイルから、リファレンスを自動で生成する機能がついたものです。使い方については、YouTubeにて公開しております。

利用法については、大まかな流れは以下のとおりとなります。

###### （１）zoteroからcsvをエクスポートする

https://www.youtube.com/watch?v=0C_GHGgeZos

###### （２）GitHubからリファレンス自動生成機能をダウンロードする

https://www.youtube.com/watch?v=t5rndVL7goU

###### （３）リファレンス自動生成機能の使い方

https://www.youtube.com/watch?v=Zoz6ZWiksbw

###### （４）タグの付け方（Zoteroデスクトップ版、web版どちらでも同じ方法でできます）

https://www.youtube.com/watch?v=noYxEoyusUc

お手数おかけしますが、ご視聴の上利用方法をご理解いただけますと幸いです。

# 編集に関わる方が編集をやる前に注意すること

1. 右上の「sync（同期）」緑矢印ボタンを押して最新のデータに更新しておくこと。（Desktop版Zoteroのみ）
これをやらないと、コンフリクト（編集の衝突）が起こる可能性があります（未確認ですが、WordやExcelのようにファイルを複数人が開いた場合のように読み取り専用とかロックが掛かりませんので起こる可能性大）
→できれば、編集を行うときには事前に皆さんに周知するとか、したほうがいいかもしれません。

2. 大規模な編集を行う場合は、不慮の編集ミスをカバーするためにも、バックアップを取れますので（またはバックアップの方法をお伝えできますので）、必要な方は事前に近森まで伝えてください。バックアップの方法は誰でもできるような内容ですが、リストアの方法も理解していないといけませんので、自信がない、というケースもあるかと思います。

# 実務の流れ

### 業績管理の流れ

1. web版ZoteroまたはDesktop版Zoteroへの入力
2. web版ZoteroまたはDesktop版Zotero上での入力内容確認
3. デスクトップ版Zoteroからのcsvファイルの出力（web版Zoteroには無い機能）
4. javascript（本機能）への落とし込みを用いて報告書（wordなど）へ提出できるようなフォーマットにし、体裁の調整
5. 出力内容確認

### 各プロセスの担当

1. 事務方の1人の担当者（岩垣さん？→事務方のみなさんで相談されて決定して下さい。）
2. authorもしくは発表者が行う（ラボメンバー全員）
3. 事務方全員（岩垣さん、東條さん、滝根さん）
4. 事務方全員（岩垣さん、東條さん、滝根さん）
5. 事務方及びauthorもしくは発表者が行う。

###### 分からない点や技術的問題・課題がありましたら遠慮なく質問ください。

### 課題とTo do

- 作業の自由度を出来るだけ少なくするプロセスは必須（入力項目のルール化）

  →チュートリアルと明確なマニュアルの作成が必要

- 現在入っているデータの体裁を整える必要あり
  →入力ルールが明確になったらみなさんで作業を進める

- 抜けや重複を防ぐため、研究者本人による確認が必要
  →システムが出来上がったらラボメンバーに方法を通知する

- javascriptの機能を報告書に沿った形に整えていくことが必要
  →tagのルールを明確化、必ず必要と思われるtagは、"年度"、"プロジェクト"、"発表日時"
  
### タグについて

- タグは、すべてアンダーバー（_）で始まるように統一しております。アンダーバーで始まらないタグ名は本システムでは利用いただけません。理由は、Zoteroでは英文論文などをchromeアドインにより新規登録したときに多くのタグが自動的に登録されることがあるからです。そして、これらのタグは本機能において不要なものです。ですから、これらのタグは本機能においては（アンダーバーで始まらないものなので）表示されないようにしております。
- 業績においてタグを加えるときは、まず頭文字としてアンダーバーから入力すれば、候補が出てきますのであとは候補を選べば、オートフィルで入力が完了します。
- 既存のタグにないタグは、新しく作ることができます。特殊な方法が必要なわけではありませんので、直接入力欄に打ち込んでください。ただし、既存のタグと１文字違いなどでかぶらないようにするためにも、既存のタグにどのようなものがあるかを前もって確認してください。
- 左上のMy Libraryをクリックすれば、左下にタグの一覧が出ます（一度も使われていないタグはここには出てきません）。または、タグ入力欄にて一文字だけアンダーバーを入力すれば、使えるタグの一覧が出ます。

# 改修について

### 技術的情報

- 今後のバージョンアップに際して、皆さんからのフィードバックが必要ですので、適宜メールなどでお願いします。

- カラムの追加削除（現在のところ87カラムのうち、12カラムのみが読み込み対象となっております）については、改修が必要となります。
![名称未設定](https://user-images.githubusercontent.com/52732083/82809349-defc2080-9ec6-11ea-8723-fd597a2cec64.jpg)


  ```
  Publication_Year
  Author
  Title
  Publication_Title
  DOI
  Url
  Date
  Pages
  Issue
  Volume
  Journal_Abbreviation
  Extra
  ```

- リファレンスを生成し終わったら、どのような条件で生成したのかをスクリーンショットなどで私にお送りください。そうすれば、次回からその条件をプルダウン選択ひとつで出せるようにすることもできます。下の部分を画像でお送りいただければ幸いです。

![名称未設定](https://user-images.githubusercontent.com/52732083/82809568-5cc02c00-9ec7-11ea-9abc-75423644422c.jpg)


### 改修のためのフィードバックあれこれ

- 「タグを変更した、タグを追加削除したい」→本システムでは、入力された内容よりtagを自動で収集しておりますので、改修の必要なくお使いいただけます。



# 開発者メモ

（１）Zoteroデスクトップ版では重複に注意すること。

インポートをしていると知らないうちに重複がどんどん増えていき、コレクションを削除するときにも「Delete collection」（正しくは「Delete Collection and Items」）を選択してしまうと、Trashがとんでもない量のレコードで溢れているなんてこともある。

Zoteroデスクトップ版では、一気に消す機能がないみたいなので、1個1個消さなければならなくなる。そんなときには、C:\Users\chikamori\Zoteroを開いて見るとsqliteファイルがあるので、それらを削除すればよい。

better-bibtex.sqlite

better-bibtex.sqlite-journal

zotero.sqlite

zotero.sqlite-journal

ただ、削除できるのはZoteroを閉じているときのみ。これらのファイルはZoteroを開いたら、また生成できるので大丈夫。空のMy Libraryができる。

Zoteroのエクスポート、インポートは今の所Zotero RDFフォーマットで成功している。今のところは、これでやるのが無難か。

（２）XMLの編集知識のある方の場合は、Exportする際は、Zoter RDFを選択することもできる。編集後、そのrdfファイルをインポートすることができる。インポートする際は、新しいフォルダを生成し、その中にインポートするというオプションが出るので、ONにしてインポートする。
