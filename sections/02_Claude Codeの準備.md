# Claude Code の準備

## 🎯 このセクションで学ぶこと

- Claude Code とは何か
- Pro プランに加入する
- Claude Code をインストールして起動する

---

## Claude Code とは

Claude Code は、Anthropic 社が提供する **AI アシスタント**です。日本語でやりたいことを伝えると、ファイルの作成・編集やブラウザ操作など、さまざまな作業を AI が代わりにやってくれます。

Claude Code は**ターミナル**という画面で動きます。ターミナルとは、PC に文字で命令を出すための画面です。黒い（または白い）背景にテキストが並んでいるだけのシンプルな画面ですが、怖いものではありません。このガイドで使うのは「コマンドをコピペして Enter を押す」程度の操作だけです。

## Step 1: Claude Pro プランに加入する

Claude Code を使うには、Claude の **Pro プラン**（月額 $20、2026 年 3 月時点）への加入が必要です。

1. ブラウザで [claude.ai](https://claude.ai) にアクセスする
2. アカウントを作成する（メールアドレスまたは Google アカウント）
3. 画面の案内に従って **Pro プラン**を選択し、支払い情報を入力する

> 💡 Pro プランに加入すると、ブラウザ版の Claude（チャット AI）も使えるようになります。Claude Code はその機能の一部です。

## Step 2: Claude Code をインストールする

### Mac の場合

1. **ターミナルを開く**
   - `Command + Space` で Spotlight を開き、「ターミナル」と入力して Enter を押します
   - 黒い背景に文字が並んだ画面が開きます。ここにコマンド（命令文）を入力していきます

2. **以下のコマンドをコピーしてターミナルに貼り付け、Enter を押す**

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

これは「Claude Code のインストールスクリプトをダウンロードして実行する」コマンドです。

### Windows の場合

1. **PowerShell を開く**
   - スタートメニューで「PowerShell」と検索して開きます

2. **以下のコマンドをコピーして貼り付け、Enter を押す**

```powershell
irm https://claude.ai/install.ps1 | iex
```

> ⚠️ Windows では事前に **Git for Windows** が必要です。インストールされていない場合は [git-scm.com](https://git-scm.com/downloads/win) からダウンロードしてください。

## Step 3: このリポジトリを clone する

このガイドのリポジトリには、ドキュメント作成に必要な Skills（AI への作業指示書）がすでに入っています。以下のコマンドでダウンロードしましょう。

**Mac の場合:**

```bash
git clone https://github.com/yotaro0616/playwright-manual-guide.git ~/Desktop/playwright-manual-guide
```

> ⚠️ `git` が使えないと言われた場合は、「インストールしますか？」というダイアログが表示されることがあります。「インストール」を選んで完了後、もう一度上のコマンドを実行してください。ダイアログが出ない場合は、ターミナルで `xcode-select --install` を実行してください。

**Windows の場合:**

```powershell
git clone https://github.com/yotaro0616/playwright-manual-guide.git $HOME\Desktop\playwright-manual-guide
```

> ⚠️ `git` が使えない場合は、[git-scm.com](https://git-scm.com/downloads/win) から Git for Windows をインストールしてください。

これは「GitHub からリポジトリをダウンロードしてデスクトップに保存する」コマンドです。

次に、ダウンロードしたフォルダに移動します。

**Mac の場合:**

```bash
cd ~/Desktop/playwright-manual-guide
```

**Windows の場合:**

```powershell
cd $HOME\Desktop\playwright-manual-guide
```

`cd` は「change directory（フォルダを移動する）」の略です。Claude Code は、このコマンドで移動した先のフォルダを作業場所として使います。

## Step 4: Claude Code を起動する

フォルダに移動できたら、以下のコマンドで Claude Code を起動します。

```bash
claude
```

初回起動時は認証が求められます。画面の指示に従い、ブラウザで Claude のアカウントにログインしてください。

認証が完了すると、ターミナルに入力欄が表示されます。ここにテキストを入力して Enter を押すと、Claude Code に指示を送れます。

> ⚠️ `command not found: claude` と表示された場合は、ターミナルを一度閉じて開き直してください。それでも解決しない場合は、インストールコマンドをもう一度実行してみてください。

---

## ✨ まとめ

- Claude Code は、ターミナルで動く AI アシスタント
- 利用には Claude **Pro プラン**（月額 $20、2026 年 3 月時点）への加入が必要
- インストールはコマンド 1 行で完了。`claude` コマンドで起動する

---

次のセクションでは、Claude Code の基本的な使い方と、プロジェクトの設定ファイルについて学びます。
