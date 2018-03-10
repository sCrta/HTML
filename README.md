# 超初心者向け　Webページ作成方法
パソコンのブラウザで何か表示してみたい人向けにメモを残しておきます。

### はじめに
初心者でも簡単にWebページ作成ができるので、下記の手順でチャレンジしてみてください。

### 超初級のサンプルページを作成してみる
1. 新規の作業フォルダを作成する

    `名前は適当に「workspace」とか。どこに作成したら良いかわからない人は、ドキュメントの下に作ればOK。`

2. 1の作業フォルダの中にテキストファイルを新規作成

    `名前は適当に。「index.txt」とか。`
3. 作成したテキストに文字を入力して上書き保存

    `文字はなんでも。「Hello World.」とか。`
4. 2のテキストファイルの拡張子を「.html」に変更

    `「index.txt」を「index.html」に変更すればOK`
5. 拡張子「.html」をダブルクリック 

    `入力した文字がブラウザに表示されるはず。`

**おめでとうございます！パソコン初心者から一歩成長しました。**


### サンプルページを編集してみる
「.html」ファイルを編集します。「.html」は、右クリックで「プログラムから開く→メモ帳」を選択して編集可能です。

`今までの拡張子「.txt」は、ダブルクリックで編集できましたが、「.html」はブラウザが開いてしまうため、編集できません。`

#### STEP1 正しいHTMLの書き方を理解しよう
編集可能になったら、下記のサンプルをコピー＆ペーストし保存し、再度ブラウザで表示してみてください。
```html
<html>
    <body>
        Hello World.
    </body>
</html>
```
ブラウザのメイン画面に「Hello World.」が表示されましたね。

```
表示される文字は先ほどと同じですが、書いたものは多いですね。
実は先ほどのサンプルは「正しくないHTML」でした。
拡張子が「.html」のため、ブラウザが自動的に補完してページを表示してくれていたのです。
この書き方がHTMLの超基本構造になります。
最初に「<html>」、最後に「</html>」を書くことで、このプログラムがHTMLであることを示しています。
表示させたい文字（Hello World.）を「<body>」と「</body>」で囲うことでブラウザに表示させたい文字を指定しています。
```

#### STEP2　タブにタイトルを表示してみる
では次に、ブラウザのタブに文字を表示させてみます。
```html
<html>
    <head>
        <title>
            Tab Title
        </title>
    </head>
    <body>
        Hello World.
    </body>
</html>
```
ブラウザのタブに「Tab Title」、ブラウザのメイン画面に「Hello World.」が表示されましたね。

#### STEP3 本文に見出しをつけてみる
「h1」のタグで見出しをつけることができます。

```html
<html>
    <head>
        <title>
            Tab Title
        </title>
    </head>
    <body>
        <h1>見出し1</h1>
        <p>Hello World.</p>
    </body>
</html>
```
同時に普通の文は「p」タグをつけておきましょう。

`ページのデザインを編集したくなった時に、この「p」タグが役立ちます。改行したいときにも使えます。`

ちなみに見出しの大きさは、番号によって選べます。


```html
<html>
    <head>
        <title>
            Tab Title
        </title>
    </head>
    <body>
        <h1>見出し1</h1>
        <h2>見出し2</h2>
        <h3>見出し3</h3>
        <h4>見出し4</h4>
        <h5>見出し5</h5>
        <h6>見出し6</h6>
        <p>Hello World.</p>
    </body>
</html>
```

#### STEP4 本文にボタンをつけてみる
ボタンをつけてみましょう。

`特に何も設定していないため、ボタンを押下しても何も起こりません。今はまだ飾りです。押下して何かイベントを起こす話はまた後日…`
```html
<html>
    <head>
        <title>
            Tab Title
        </title>
    </head>
    <body>
        <h1>見出し1</h1>
        <p>Hello World.</p>
        <button>Button</button>
    </body>
</html>
```

#### STEP5 本文に表を作成してみる
「table」タグで表を作ってみましょう
```html
<html>
    <head>
        <title>
            Tab Title
        </title>
    </head>
    <body>
        <h1>見出し1</h1>
        <p>Hello World.</p>
        <button>Button</button>
        <table>
            <tr>
                <td>1行1列</td>
                <td>1行2列</td>
                <td>1行3列</td>
            </tr>
            <tr>
                <td>2行1列</td>
                <td>2行2列</td>
                <td>2行3列</td>
            </tr>
        </table>
    </body>
</html>
```
「tr」タグで行を指定、「td」タグで列を指定できました。

このままでは表っぽくないですね、青い線を引いてみます。
```html
<html>
    <head>
        <title>
            Tab Title
        </title>
        <style>
            td {border: 1px blue solid;}
        </style>
    </head>
    <body>
        <h1>見出し1</h1>
        <p>Hello World.</p>
        <button>Button</button>
        <table>
            <tr>
                <td>1行1列</td>
                <td>1行2列</td>
                <td>1行3列</td>
            </tr>
            <tr>
                <td>2行1列</td>
                <td>2行2列</td>
                <td>2行3列</td>
            </tr>
        </table>
    </body>
</html>
```
見た目を変えたいときには、「style」タグを使用します。

今回は、「td」タグに対して「border(線)の太さ1px、色blue、線の種類solid(実線)」を設定しています。

まだ表っぽくないですね。線の間の隙間を埋めてみます。

```html
<html>
    <head>
        <title>
            Tab Title
        </title>
        <style>
            table {border-collapse: collapse;}
            td {border: 1px blue solid;}
        </style>
    </head>
    <body>
        <h1>見出し1</h1>
        <p>Hello World.</p>
        <button>Button</button>
        <table>
            <tr>
                <td>1行1列</td>
                <td>1行2列</td>
                <td>1行3列</td>
            </tr>
            <tr>
                <td>2行1列</td>
                <td>2行2列</td>
                <td>2行3列</td>
            </tr>
        </table>
    </body>
</html>
```
「table」タグに隙間いらないよと設定してあげます。

***おめでとうございます！いつの間にかCSS言語も習得しました***

CSS言語とは、「style」タグの中に書いた言語です。

ここだけ少し書き方が異なりますね。

HTML言語とCSS言語の組み合わせで、Webページ作成は大体できます。

HTMLの基本的なタグは、下記のサイトを参照することをおすすめします。

http://www.tagindex.com/html_tag/elements/ 


### おわりに
パソコンが扱えることは、この先役に立つ機会は多いと思います。

この解説がWebページ作成の一歩を後押しできたなら幸いです。