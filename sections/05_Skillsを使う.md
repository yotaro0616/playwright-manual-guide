# Skills を使う

## 🎯 このセクションで学ぶこと

- Skills（スキル）とは何か
- このリポジトリに含まれる 3 つの Skills を確認する
- `/スキル名` でスキルを呼び出す方法

---

## Skills とは

**Skills** は、Claude Code で使える**再利用可能なプロンプトテンプレート**です。

たとえば、「Web アプリを探索して調査レポートを作って」という長い指示を毎回入力するのは面倒です。Skills を使えば、この指示を `SKILL.md` というファイルに保存しておき、`/web-app-explorer` と入力するだけで呼び出せます。

## このリポジトリに含まれる 3 つの Skills

このリポジトリには、ドキュメント作成に必要な 3 つの Skills がすでに入っています。セクション 2 の手順でこのリポジトリを clone していれば、**あなたがファイルを作成する必要はありません**。

| スキル名 | コマンド | やること |
|---------|---------|---------|
| web-app-explorer | `/web-app-explorer` | Web アプリを探索して調査レポートを作成 |
| operation-manual-creator | `/operation-manual-creator` | 調査結果からマニュアルを生成 |
| manual-screenshot-capture | `/manual-screenshot-capture` | マニュアルの指示に従いスクショを撮影 |

## スキルファイルの構造

3 つの Skills は `.claude/skills/` フォルダに配置されています。

```
.claude/
└── skills/
    ├── web-app-explorer/
    │   └── SKILL.md
    ├── operation-manual-creator/
    │   └── SKILL.md
    └── manual-screenshot-capture/
        └── SKILL.md
```

> 💡 `.claude` フォルダは先頭にドット（`.`）が付いているため、通常はフォルダ一覧に表示されません。ターミナルで `ls -a` を実行すると確認できます。

各 SKILL.md の中身は、Claude Code への詳細な作業指示書です。あなたが中身を理解する必要はありません。Claude Code がこの指示を読んで自動的に動いてくれます。

> 💡 各スキルの詳しい内容に興味がある場合は、GitHub 上で `.claude/skills/` フォルダを開いて読むことができます。

## スキルの呼び出し方

Claude Code 起動中に `/スキル名` と入力するだけです。

```
/web-app-explorer
```

スキル名の後に追加の指示を付けることもできます。

```
/web-app-explorer 管理者ロールだけ探索して
```

> 💡 確認方法: Claude Code に「使えるスキルを教えて」と聞くと、認識されているスキルの一覧を表示してくれます。

---

## ✨ まとめ

- **Skills** は再利用可能なプロンプトテンプレート。`/スキル名` で呼び出せる
- このリポジトリには 3 つの Skills がすでに入っている（自分で作成する必要なし）
- 次のセクションからこの 3 つの Skills を使って実際にドキュメントを作成する

---

次のセクションでは、さっそく web-app-explorer を使って Web アプリを探索します。
