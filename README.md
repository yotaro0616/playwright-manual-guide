# Claude Code × Playwright ドキュメント作成ガイド

Web アプリの操作マニュアルを作るのに、画面を1つずつ開いてメモを取り、手順を書き起こし、スクリーンショットを1枚ずつ撮っていませんか？

このリポジトリでは、**Claude Code**（AI アシスタント）と **Playwright**（ブラウザ自動操作ツール）を使って、この一連の作業を AI に任せる方法を紹介します。

## クイックスタート

> Claude Code、Node.js 18 以上が必要です。初めての方は[セクション 2](sections/02_Claude%20Codeの準備.md) から順に進めてください。

```bash
# 1. リポジトリを clone
git clone https://github.com/yotaro0616/playwright-manual-guide.git
cd playwright-manual-guide

# 2. Playwright MCP を登録
claude mcp add playwright -- npx @playwright/mcp@latest

# 3. Claude Code を起動して 4 つの Skills を順に実行
claude
# → /setup                 （アプリ情報を設定）
# → /explore               （アプリを探索）
# → /create-manual          （マニュアルを生成）
# → /capture-screenshots    （スクショを撮影）
```

## できるようになること

| 作業 | 使う Skill | やること |
|------|-----------|---------|
| **設定** | `/setup` | CLAUDE.md にアプリ情報を設定し、プロジェクト構造を作成 |
| **調査** | `/explore` | Web アプリの画面・機能を AI が自動で巡回し、調査レポートを作成 |
| **執筆** | `/create-manual` | 調査結果をもとに操作マニュアルを自動生成 |
| **撮影** | `/capture-screenshots` | マニュアルに必要なスクリーンショットを自動撮影・挿入 |

## 前提条件

- PC（Mac / Windows / Linux）、インターネット接続、クレジットカード
- Claude Pro プラン（月額 $20）
- Node.js 18 以上
- プログラミング経験は不要です

## セクション一覧

### 準備（セクション 1〜3）

1. [このガイドについて](sections/01_このガイドについて.md) — 全体像と前提条件
2. [Claude Code の準備](sections/02_Claude%20Codeの準備.md) — Pro プラン加入、インストール、clone
3. [基本操作と CLAUDE.md](sections/03_基本操作とCLAUDE.md.md) — プロンプトの送り方、プロジェクト設定

### 本題（セクション 4〜5）

4. [MCP で Playwright に接続する](sections/04_MCPでPlaywrightに接続する.md) — ブラウザ自動操作の設定
5. [Skills を使う](sections/05_Skillsを使う.md) — 4 つの Skills の確認と使い方

### 実践（セクション 6〜8）

6. [Web アプリを探索する](sections/06_Webアプリを探索する.md) — 初期設定と調査スキルの実践
7. [操作マニュアルを作成する](sections/07_操作マニュアルを作成する.md) — 執筆スキルでマニュアルを自動生成
8. [スクリーンショットを自動撮影する](sections/08_スクリーンショットを自動撮影する.md) — 撮影スキルでスクショを一括撮影

## リポジトリの構造

```
playwright-manual-guide/
├── README.md                  # このファイル
├── CLAUDE.md                  # テンプレート（/setup で対話的に設定）
├── sections/                  # ガイド本文（セクション 1〜8）
└── .claude/
    ├── settings.json
    └── skills/                # 4 つの Skills（clone すれば即使える）
        ├── setup/SKILL.md
        ├── explore/SKILL.md
        ├── create-manual/SKILL.md
        └── capture-screenshots/SKILL.md
```

## ライセンス

MIT
