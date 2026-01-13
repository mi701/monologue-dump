# Webサイト公開手順書 (GitHub + Netlify)

このガイドでは、作成したWebサイトを世界中に公開するための手順を説明します。
英語の画面での操作が必要ですが、この通りに進めれば大丈夫です。

## 手順 1: ローカルでの準備 (私がやります)

まず、あなたのパソコン上でファイルを「Git」というツールで管理できる状態にします。
これは私がコマンドで行いますので、**あなたは何もする必要はありません**。

> (私がこれから `git init` などのコマンドを実行します)

## 手順 2: GitHubで「リポジトリ」を作る

GitHub上にファイルの保存場所（リポジトリ）を作ります。

1. [GitHub](https://github.com/) にログインします。
2. 画面右上の **「+」アイコン** をクリックし、**「New repository」** を選びます。
3. **「Repository name」** の欄に、好きな名前（例: `my-blog-website`）を半角英数で入力します。
4. **「Public」** (誰でも見れる) が選ばれていることを確認します。
5. 画面一番下の **「Create repository」** (緑色のボタン) をクリックします。

## 手順 3: ファイルをアップロードする

リポジトリを作ると、いくつかコマンドが表示される画面になります。
以下のコマンドをコピーして、このチャットの入力欄に貼り付けて教えてください。
私が代わりに実行して、ファイルをアップロードします。

**コピーしてほしい部分:**
> `…or push an existing repository from the command line` と書かれている下の3行くらいのコマンド。
> 通常は以下のようになっています:
> ```bash
> git remote add origin https://github.com/ユーザー名/リポジトリ名.git
> git branch -M main
> git push -u origin main
> ```

## 手順 4: Netlifyで公開する

ファイルがGitHubに上がったら、Netlifyと連携します。

1. [Netlify](https://www.netlify.com/) にログインします。
2. 管理画面(Team Overview)で **「Add new site」** を押し、**「Import from an existing project」** を選びます。
3. **「Connect to Git provider」** という画面で **「GitHub」** を選びます。
   - 認証画面が出たら「Authorize Netlify」などをクリックして許可します。
4. リポジトリの一覧が出るので、さきほど作った **`my-blog-website`** (あなたがつけた名前) を選びます。
5. 設定画面になりますが、基本そのままでOKです。一番下の **「Deploy my-blog-website」** (青いボタン) をクリックします。

## 手順 5: 完成！

しばらく待つと、「Site deploy in progress」から「Site is live」のような表示に変わります。
画面上のほうに表示される **`https://random-name-12345.netlify.app`** のようなURLをクリックすると、スマートフォンからでもアクセスできます！

---

### ※後で更新したいときは？

記事を追加したり修正した後は、私に「GitHubに更新をプッシュして」と言っていただければ、私がコマンドを実行します。
そうすると、Netlifyが自動的に検知して、新しい内容でサイトを更新してくれます。便利です！
