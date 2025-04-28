---
title: "Chapter3-1 Clusterでログを表示しよう"
---

## Chapter3-1: Clusterでログを表示しよう

Assets/Chapter3/Chapter3-1に必要なファイルがあります

## このセクションのゴール
- コンソール上にログを出力する方法を理解する
- 自分の書いたスクリプトをclusterで動かす方法を理解する

## ログとは？

ログとは、記録という意味があります。コードの出力結果という意味で理解しても構いません。
詳しくはこちら：https://wa3.i-3-i.info/word1415.html

ログ出力の方法を覚えておくと、コードが壊れたときに原因の調査をしたり、コードが正しく動いているかどうかを確認することができます。
このチャプターでは、ログを出力し、clusterの中で確認する方法を紹介します。

## clusterでログを出す

### cluster Scriptのファイルを作成しよう

Projectタブで、「+」ボタン or 右クリックでメニューを開き、Create > cluster > ClusterScript を選択。すると、ClusterScriptファイルが作成されます。
ここでは「Chapter3-1Script」と名前を付けましょう

![](/images/chapter3-1/image1.png)

### cluster Scriptを書こう

作成したChapter3-1Scriptをダブルクリック。すると、Visual Studio Codeが立ち上がります。

![](/images/chapter3-1/image2.png)

![](/images/chapter3-1/image3.png)

では早速、Visual Studio Codeを使ってコードを書いてみましょう。
以下のコードを書いてみてください。
コードを書いたら、保存するのを忘れないでください。

```js
$.onStart(() => {
  $.log("hello cluster");
})
```
この記述について解説します。


#### $.onStartとはなにか？
この記述は、`$.onStart(()) => {`で始まり、`})`で終わる一つのグループです。
詳しくは、関数の解説をするチャプターで触れます。
今は特に深く考えず、「このグループの中に実行したいコードを書く」「このグループの中に書いた処理は、ワールドが立つと一度だけ実行される」という理解で十分です。

```js
$.onStart(() => {
  // ここに実行したい処理を書く
})
```


####  $.logとはなにか？
この記述が、このチャプターの主役です。
cluster Scriptでログを出力したい場合は、`$.log()`という記述を使います。
以下のように、`$.log(出力したい内容)`と記述することで、cluster上にログを出力することができます。

```js
$.log("このテキストがログとして出力されます")
```

### cluster Scriptを動かそう
では早速、書いたコードをclusterで動かしてみましょう。

まず、「ctrl + R」（macは「command + R」）を押して、UnityをRefreshしてください。
cluster Scriptを書いても、RefreshをしないとスクリプトがUnity上に反映されない場合があります。
正しく反映されているか確認したい場合は、Chapter3-1Scriptファイルを選択し、Inspectorにコードが表示されているかどうかを確認してください。

![](/images/chapter3-1/image5.png)

次は、空のゲームオブジェクトを作りましょう。
Hierarchyウィンドウで、「+」 or 右クリックでCreate Emptyをクリックし、空のゲームオブジェクトを作成します。
GameObjectは、Chapter3-1ScriptObjectと命名しましょう。

作ったObjectを選択し、Inspectorウィンドウに情報を表示。Add Componentをクリックし、Scriptable Itemをアタッチします。
アタッチしたScriptable ItemのSource Code Assetに、先ほど作成したcluster Scriptのファイル「Chapter3-1Script」をドラッグ&ドロップして、スクリプトを紐づけましょう。
以下のような画面になっていればよいです。

![](/images/chapter3-1/image4.png)

これでワールドの準備が完了しました。実際にclusterにワールドをアップロードしましょう。
ワールドのアップロードは普段通りで構いません。
ワールドのアップロード方法がわからない方は以下を参照してください。
https://docs.cluster.mu/creatorkit/world/upload-world/

### clusterでログを確認しよう

では、アップロードしたワールドに入ってみましょう。
ワールドに入って、コンソールを見ると、「hello cluster」と表示されます。
これが表示されていれば、正しくコードが実行されています。

![](/images/chapter3-1/image6.png)

これでログの出力ができました！
この「ログの出力」の操作は、この先のチャプターでも頻繁に使いますのでぜひ理解しておきましょう。

---
このドキュメントは、現在執筆中です。コントリビューション大歓迎です。
記事の編集をしたい場合は、以下のGitHubリポジトリでIssueを立てたりPRを投げてください。
本に執筆WorkFlowに関する改善も大歓迎です。
https://github.com/yuya-0928/JavaScriptTutorialForClusterScriptDocument