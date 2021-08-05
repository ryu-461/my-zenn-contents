---
title: "npmは本当に「Node Package Manager」の意味なのか"
emoji: "🤔"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["npm"]
published: false
---

# はじめに

Node.jsにはデフォルトでnpmというパッケージマネージャが付属します。

npmはよく「Node Package Managerの略です」といった説明がされています。しかしそれは本当に正しいのでしょうか。
一般的に「Node Package Manager」の頭文字を並べたものという認識がされているなか、先日npm-cliのGitHubリポジトリを見ていたときに興味深い説明を発見したので調べてみました。

こちらがnpmのGitHubリポジトリになります。

https://github.com/npm/cli

結論からまとめると**npmとは「npm is not an acronym」のバクロニム**であり、「Node Package Manager」の頭文字を表しているものではないとのことです。これだけ聞いてもあまりピンとこないので、この記事でnmの主張や略式にまつわる文化についても掘り下げてみます。

またnpmといえばのWebサイト[npm.js](https://www.npmjs.com/)の左上にnpmという文字列から3語の造語を生成して並べるトリックが有名です。

![npmトップページのIF](/images/what-npm-means/image01.gif)
***クリックのたびにnpmのバクロニムが表示されます***

 10回クリックすることで意味深なGitHubのリポジトリページへ遷移する仕様となっています。
 これもnpmの由来、意味に関係するのでしょうか。

# npmの主張

GitHubリポジトリのREADMEに以下の見出しがあり、なぜnpmがnpmと呼ばれるのかについての注釈がありました。

以下、README内「FAQ on Branding」からの引用となります。

> Is "npm" an acronym for "Node Package Manager"?

> Contrary to popular belief, npm is not in fact an acronym for "Node Package Manager"; It is a recursive bacronymic abbreviation for "npm is not an acronym" (if the project was named "ninaa", then it would be an acronym).

日本語に訳すと以下のようになります。

Q. "npm "は "Node Package Manager "の頭文字ですか。

A. 一般的に信じられていることとは異なり、npmは実際には「Node Package Manager」の頭文字ではありません。もしプロジェク名が「ninaa」なら頭文字といえます。

早速、「Node Package Manager」の頭文字を並べたもの ≠ npmと主張しています。さっそく否定から入ったのでこれには驚きました。ずっと頭文字を並べたものだと思っていたので公式リポジトリ内で弁明していることがとても衝撃的でした。

要約するとnpmとは。
> npm is not an acronym（npmはacronymではない）

を再帰的に表現したものなんですね。

要するに、npnはNとのことです。バクロニムというやや少し難しい言葉がでてきましたね。

# バクロニムとは

バクロニム（backronym）は日本語で逆頭字語と表されます。また頭文字のことをアクロニムといい、アクロニムを再帰的に表すとバクロニムとなります。言葉だけだと少しわかりにくいので例を挙げてみます。

バクロニムの有名な例として「SOS」というものがあります。本来モールス信号であるものが（**S**ave **O**ur **S**hip）や（**S**ave **O**ur **S**ouls）といった後付の解釈によって表されます。本来意味のない言葉が後付によって頭文字のような意味をもつ。つまり一種の言葉遊びのようなものですね。

また。頭文字（アクロニム）は比較的イメージしやすいです。複数の単語から成り立つ言葉があったときにそれぞれの頭文字を並べたものになります。バクロニムの逆といった感じでしょうか。

普段目にする頭文字の例として、以下のようなものがあります。

- IT（**I**nformation **T**echnology）
- RPA（**R**obotic **P**rocess **A**utomation）
- IOC（**I**nternational **O**lympic **C**ommittee）

これらはそのまま頭文字（アクロニム）と呼ばれます。この流れからnpmも「**N**ode **P**ackage **M**anager」かと思われがちですが、これが面白いことにnpmは「npm is not an acronym」のバクロニムであると主張しています。これが本記事で取り上げる内容に繋がります。

# 頭文字と再帰的頭字語の違いとは


頭文字は日本で良くみる略式になりますが、それと対象的な位置にあるのが再帰的頭字語（recursive acronym）というものです。

これは海外で一時期、略語でありながら皮肉、自虐的に略するような文化があったことに由來します。

再帰的頭字語の例だとプログラミング言語のPHPの由来が有名です。
[PHPのドキュメントの冒頭](https://www.php.net/manual/ja/intro-whatis.php)に以下の説明があります。

> PHP (PHP: Hypertext Preprocessor を再帰的に略したものです) は、広く使われているオープンソースの汎用スクリプト言語です。

PHPはPHP: Hypertext Preprocessorを再帰的に略したものという説明をみて違和感を感じる人も少なくないです。頭文字をならべる感覚（アクロニム）で見ていくと、PHPのHPは直感的にわかるけど、先頭にあるPは一体何なんだろうという考えになり、ループに陥る感覚を覚えます。このような言葉を再帰的頭字語（recursive acronym）と呼びます。

再帰的頭字語の有名なものとしてYAMLやGNU、LAMEがあります。

- YAML（YAML Ain't a Markup Language）YAMLはマークアップ言語じゃないの意。
- GNU（GNU's Not UNIX！）GNUはUNIXではないの意。
- PNG（LAME Ain't an Mp3 Encoder）LAMEはMP3のエンコーダーではないの意。

上に挙げたもののように言葉遊びにユーモアがありつつ皮肉がこめられているものが多くあります。

再帰的頭字語と頭文字を比較すると以下のようになります。

・再帰的頭字語（アクロニム）。
・頭文字（バクロニム）

# npmの本質とは

FAQには合わせて以下のような説明があります。

>  The precursor to npm was actually a bash utility named "pm", which was the shortform name of "pkgmakeinst" - a bash function that installed various things on various platforms. If npm were to ever have been considered an acronym, it would be as "node pm" or, potentially "new pm".

> npmの前身は、実際には "pm "という名前のbashユーティリティで、これは "pkgmakeinst "というbash関数の短縮形の名前でした。もしnpmの頭文字を取るとしたら、"node pm "か、あるいは "new pm "になるでしょう。

npmの前身となるパッケージマネージャの名前が「pm」というものだったようです。npmを頭文字をとったものとするならnpmは「node pm」「new pm」のようになると主張しています。

このことから今はNode.jsに限らす、JavaScriptのパッケージマネージャとしての立ち位置にあるnpmがNodeに縛られないパッケージマネージャなんだと主張しているようち感じられます。このように見ていくとnpmの頭文字じゃないを再帰的に略したものがnpmであるという説明もやや皮肉が含まれていて面白いですね。

また、冒頭で紹介したnpmのトリックなのですが、クリックして遷移するリポジトリ[GitHub - npm/npm-expansions](https://github.com/npm/npm-expansions)ではnpmのバクロニムをプルリクエストにて募集しています。記事執筆時点で800以上のバクロニムが追加されていて驚きました。ここに登録されているものがトップページにてランダム表示されるようです。

数多くのバクロニムがありますが、私は特に以下のバクロニムが気に入りました。

> Neverending Programming Mistakes

npmの遊び心が感じられるリポジトリで寄せられたものを見ているだけでも面白いです。

# おわりに

今回はnpmのもつ意味や由来について調べてまとめてみました。今までただ、Node Package Managerの頭文字を取ったものだと認識していましたが、ただそれだけでなく皮肉的な意味合いもあり面白いと感じました。

再帰的略語が飛び交うIT業界で仕事をしていると、なぜこのような名前にしたのか不思議に感じる技術を目にすることが多くあります。実際何気なく見ているものでも調べてみるとその背景には開発者の思いや、考え方が現れており、多くの発見があるように感じます。

また気になったことを調べることで得られる発見により技術がもっと好きになりますね。

最後まで読んでいただきありがとうございました。