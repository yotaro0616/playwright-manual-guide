# MCP で Playwright に接続する

## 🎯 このセクションで学ぶこと

- MCP とは何か
- Playwright MCP を設定して Claude Code からブラウザを操作できるようにする
- 実際にスクリーンショットを撮って動作を確認する

ここからがこのガイドの本題です。Claude Code に**ブラウザ操作**の能力を追加し、Web アプリのドキュメント作成を自動化する準備をします。

---

## MCP とは

**MCP**（Model Context Protocol）は、Claude Code に**外部ツールを接続する仕組み**です。

Claude Code は単体でもファイル操作やコマンド実行ができますが、MCP を使うと「ブラウザ操作」のような追加の能力を持たせることができます。

このガイドでは、**Playwright MCP** を接続します。Playwright は Microsoft 社が開発したブラウザ自動操作ツールで、これを接続すると Claude Code が Web ブラウザを開いて画面を見たり、ボタンをクリックしたり、スクリーンショットを撮ったりできるようになります。

## Step 1: Node.js をインストールする

Playwright を動かすには **Node.js**（バージョン 18 以上）が必要です。

> 💡 Node.js はプログラミング言語の実行環境ですが、あなたがプログラムを書く必要はありません。Playwright を裏側で動かすために必要なだけです。

まず、既にインストールされているか確認しましょう。ターミナルで以下を実行してください。

```bash
node -v
```

`v18` 以上の数字（例: `v22.14.0`）が表示されれば、既にインストール済みです。**Step 2 に進んでください。**

`command not found` と表示された場合、またはバージョンが `v18` 未満の場合は、以下の手順でインストールします。

1. ブラウザで [nodejs.org](https://nodejs.org/) にアクセスする
2. **LTS**（推奨版）と書かれたボタンをクリックしてダウンロード
3. ダウンロードしたファイルを開き、画面の指示に従ってインストール

インストール後、ターミナルを一度閉じて開き直し、もう一度 `node -v` を実行してバージョンが表示されれば OK です。

## Step 2: Playwright MCP を登録する

ターミナルで以下のコマンドを実行します（Claude Code は起動していない状態で OK です）。

```bash
claude mcp add playwright -- npx @playwright/mcp@latest
```

これは「Claude Code に Playwright MCP サーバーを登録する」コマンドです。`--` の後ろが実際に起動されるプログラムです。そのままコピー＆ペーストして実行してください。一度実行すれば設定が保存されるので、次回以降は不要です。

## Step 3: 接続を確認する

Claude Code を起動（または再起動）します。

```bash
claude
```

起動時のメッセージに以下が含まれていれば接続成功です。

```
playwright: connected
```

> ⚠️ `playwright: failed to connect` と表示された場合は、Node.js のバージョンが 18 未満の可能性があります。`node -v` で確認してください。

## Step 4: スクリーンショットを撮ってみる

接続できたら、さっそく試してみましょう。Claude Code に以下のように入力してください。

```
https://example.com を開いてスクリーンショットを撮って、screenshot.png として保存して
```

Claude Code が Playwright を使ってブラウザを自動操作し、スクリーンショットが保存されます。プロジェクトフォルダに `screenshot.png` ができていれば成功です。

> 💡 このとき、画面上に実際のブラウザが表示されるわけではありません。Playwright は「見えないブラウザ」を裏側で動かしています。

## Playwright MCP で使えるツール

Claude Code から Playwright を使うと、以下のような操作ができます。セクション 6〜8 の Skills はこれらを組み合わせて自動的に動作します。

| ツール | できること |
|--------|-----------|
| `browser_navigate` | 指定した URL に移動する |
| `browser_snapshot` | ページの構造を読み取る |
| `browser_click` | ボタンやリンクをクリックする |
| `browser_fill_form` | フォームにテキストを入力する |
| `browser_take_screenshot` | スクリーンショットを撮影する |

> 💡 あなたがこれらのツール名を覚える必要はありません。次のセクション以降で使う Skills が、適切なツールを自動で選んで実行します。

---

## ✨ まとめ

- **MCP** は Claude Code に外部ツールを接続する仕組み
- `claude mcp add playwright` コマンド 1 つで Playwright を接続できる
- 接続すると、Claude Code がブラウザの操作やスクリーンショット撮影をできるようになる
- これがこのガイドの核心技術。セクション 6〜8 の Skills はすべてこの Playwright を使って動作する

---

次のセクションでは、ドキュメント作成に使う 3 つの Skills を配置します。
