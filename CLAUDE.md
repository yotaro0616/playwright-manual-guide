# ドキュメント作成プロジェクト

## アプリ情報

<!-- ここにあなたのアプリの情報を記載してください -->

- URL: https://your-app.example.com/login
- アカウント:
  - メールアドレス: user@example.com
  - パスワード: password123

<!-- 複数ロールがある場合は追加 -->
<!-- - 管理者アカウント: -->
<!--   - メールアドレス: admin@example.com -->
<!--   - パスワード: admin123 -->

## 安全制約

- データの削除は行わない
- 設定の変更は行わない

## 成果物

| ファイル | 内容 |
|---------|------|
| `exploration/findings.md` | アプリ探索結果 |
| `docs/` | 操作マニュアル |
| `assets/` | スクリーンショット |

## ワークフロー

1. `/web-app-explorer` — アプリを探索して調査レポートを作成
2. `/operation-manual-creator` — 調査結果からマニュアルを生成
3. `/manual-screenshot-capture` — マニュアルの📸指示からスクショを自動撮影
