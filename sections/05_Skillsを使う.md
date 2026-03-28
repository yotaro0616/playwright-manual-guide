# Skills を使う

## 🎯 このセクションで学ぶこと

- Skills（スキル）とは何か
- このリポジトリに含まれる 4 つの Skills を確認する
- `/スキル名` でスキルを呼び出す方法

---

## Skills とは

**Skills** は、Claude Code で使える**再利用可能なプロンプトテンプレート**です。

たとえば、「Web アプリを探索して調査レポートを作って」という長い指示を毎回入力するのは面倒です。Skills を使えば、この指示を `SKILL.md` というファイルに保存しておき、`/explore` と入力するだけで呼び出せます。

## このリポジトリに含まれる 4 つの Skills

このリポジトリには、ドキュメント作成に必要な 4 つの Skills がすでに入っています。セクション 2 の手順でこのリポジトリを clone していれば、**あなたがファイルを作成する必要はありません**。

| スキル名 | コマンド | やること |
|---------|---------|---------|
| setup | `/setup` | プロジェクトの初期設定（CLAUDE.md にアプリ情報を記入） |
| explore | `/explore` | Web アプリを探索して調査レポートを作成 |
| create-manual | `/create-manual` | 調査結果からマニュアルを生成 |
| capture-screenshots | `/capture-screenshots` | マニュアルの指示に従いスクショを撮影 |

4 つの Skills は、この順番で使うことを想定しています。

```
/setup → /explore → /create-manual → /capture-screenshots
```

> 💡 各スキルは独立しているので、1 つだけ使うこともできます。たとえば、既にマニュアルがある場合は `/capture-screenshots` だけ使えます。

## スキルファイルの構造

4 つの Skills は `.claude/skills/` フォルダに配置されています。

```
.claude/
└── skills/
    ├── setup/
    │   └── SKILL.md
    ├── explore/
    │   └── SKILL.md
    ├── create-manual/
    │   └── SKILL.md
    └── capture-screenshots/
        └── SKILL.md
```

> 💡 `.claude` フォルダは先頭にドット（`.`）が付いているため、通常はフォルダ一覧に表示されません。ターミナルで `ls -a` を実行すると確認できます。

各 SKILL.md の中身は、Claude Code への詳細な作業指示書です。あなたが中身を理解する必要はありません。Claude Code がこの指示を読んで自動的に動いてくれます。

> 💡 各スキルの詳しい内容に興味がある場合は、GitHub 上で `.claude/skills/` フォルダを開いて読むことができます。

## スキルの呼び出し方

Claude Code 起動中に `/スキル名` と入力するだけです。

```
/explore
```

スキル名の後に追加の指示を付けることもできます。

```
/explore 管理者ロールだけ探索して
```

> 💡 確認方法: Claude Code に「使えるスキルを教えて」と聞くと、認識されているスキルの一覧を表示してくれます。

---

## ✨ まとめ

- **Skills** は再利用可能なプロンプトテンプレート。`/スキル名` で呼び出せる
- このリポジトリには 4 つの Skills がすでに入っている（自分で作成する必要なし）
- `/setup` → `/explore` → `/create-manual` → `/capture-screenshots` の順で使う
- 次のセクションから、まず `/setup` で初期設定を行い、実際にドキュメントを作成する

---

次のセクションでは、さっそく `/setup` でプロジェクトを設定し、`/explore` で Web アプリを探索します。
