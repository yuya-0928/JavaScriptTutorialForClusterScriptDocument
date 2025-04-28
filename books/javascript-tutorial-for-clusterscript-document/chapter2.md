---
title: "環境構築"
---

## Unityの環境構築がまだの場合
Unityのダウンロード方法・Unityの環境構築については、以下のリンクからをClustesGuideを確認してください。
https://creator.cluster.mu/cck-worldcreatetutroial-home/
ClustesGuideの「第1.5回：Unityを導入する」から「第2回：Cluster Creator Kitの導入方法」までを完了すればUnityの準備は完了です。

以下の2つができていれば、最低限の準備は完了です。
- Unity Hubをダウンロードする
- Unity Hubを経由して、Unity 2021.3.4f1をダウンロードする
	- Unityダウンロード時は、必要な追加モジュールをダウンロードしておく（Android Build Supportなど）

## チュートリアルプロジェクトをダウンロードしてUnityで開こう
このチュートリアルでは、事前に用意したUnityプロジェクトを実際に触りながら、JavaScriptについて学びます。

Unityプロジェクトは、GithubというWebサービスで配布をしています。

### Githubからプロジェクトをダウンロードしよう
以下のリンクにアクセスしてください。
https://github.com/yuya-0928/JavaScriptTutorialForClusterScriptUnityProject

こちらのページで、緑色の｢Code｣ボタンをクリックし、出てくるメニューのボタンの中の｢Download ZIP｣を選択して、プロジェクトをダウンロードしてください。

![Githubの画面](/images/chapter2/image3.png)

Zip形式でダウンロードされますので、Zipを解凍して、自分の好きな場所にファイルを保存してください。

### UnityHubからダウンロードしたプロジェクトを開こう

ダウンロードしたファイルをUnityHubから開きましょう。
UnityHubを開き、画面上部のメニューから、Add > Add project from disk を選択し、先ほどダウンロードしたプロジェクトを選択します。
先ほどダウンロードしたプロジェクトを選択する場合、JavaScriptTutorialForClusterScriptUnityProject-mainの下にもう一つJavaScriptTutorialForClusterScriptUnityProject-mainというディレクトリがあります。そちらを選択してください

![UnityHub](/images/chapter2/image4.png)

すると、JavaScriptTutorialForClusterScriptUnityProject-mainというプロジェクトがUnityHubに追加されるので、それを選択してください。
Unityが開きます。


## エディタを準備しよう
コードを書くソフトウェアのことエディタと表現しています。
このドキュメントでは、自由なエディタを使って開発を進められるように書いています。
自分の使いやすいエディタを使ってください。

このチュートリアルでは、Visual Studio Codeを前提に解説を進めていきます。
以下の項では、Visual Studio Codeの解説と導入の手順を説明します。

Unityは標準でVisual Studio、Visual Studio Code (VSCode)、JetBrains Riderのエディタが利用できます。いくつかのエディタについては解説を省きますが、もし興味がありましたら調べてみると良いと思います。
https://docs.unity3d.com/ja/2021.3/Manual/Preferences.html#external-tools

### Visual Studio Codeとは？

数あるコードエディタソフトの一つです。様々な拡張機能を導入することで便利に開発を進めることができます。

### Visual Studio Codeのインストール方法

Visual Studio Codeは以下のリンクからダウンロードできます
https://code.visualstudio.com/download

![ダウンロード画面](/images/chapter2/image1.png)

Windowsを使っている場合はWindowsのロゴが書かれているボタンをクリックしてください。
Macを使っている場合はまMacのロゴが書かれているボタンをクリックしてください。

ダウンロードが終わったら、アプリを起動してみて、実際に使えるかどうか確認をしてみてください。

### UnityでVisual Studio Codeを利用できるようにするための設定

Unityはデフォルトだと、Visual Studioという別のエディタを使うように設定がされています。Visual Studio Codeを使う場合は、この設定を変更する必要があります。

Unityを開き、画面上部から Edit > Preferences > External Toolsの中にある、External Script Editorの設定を変更します。

プルダウンを選択すると、選択候補の中にVisual Studio Codeがあるので、そちらを選択してください。
もしVisual Studio Codeの項目がない場合は、Unityを再起動してみてください。

![VisualStudioCodeの設定画面](/images/chapter2/image2.png)

## 環境構築完了!
ここまでの手順が全てできたら、環境構築は完了です。
次の章からは、実際にコードを書きながらJavaScriptを勉強していきましょう!

---
このドキュメントは、現在執筆中です。コントリビューション大歓迎です。
記事の編集をしたい場合は、以下のGitHubリポジトリでIssueを立てたりPRを投げてください。
本に執筆WorkFlowに関する改善も大歓迎です。
https://github.com/yuya-0928/JavaScriptTutorialForClusterScriptDocument