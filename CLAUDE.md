# ドキュメント作成プロジェクト

<!-- /setup を実行すると、以下のセクションが対話的に設定されます -->

## アプリ情報

<!-- 例: https://your-app.com/login -->
- URL: （/setup で設定）
- アカウント:
  <!-- 例: 管理者: admin@example.com / password123 -->
  - ロール名:
    - メールアドレス:
    - パスワード:

## ロール

<!-- 例: 管理者、一般ユーザー など -->
- （/setup で設定）

## 安全制約

- データの削除は行わない
- 設定の変更は行わない

## 出力先

| 成果物 | パス |
|--------|------|
| 探索結果 | exploration/findings.md |
| マニュアル | docs/{role}/manual.md |
| 画像 | assets/{role}/images/ |

## ワークフロー

1. `/setup` — プロジェクトの初期設定（アプリ情報の記入）
2. `/explore` — アプリを探索して調査レポートを作成
3. `/create-manual` — 調査結果からマニュアルを生成
4. `/capture-screenshots` — マニュアルの📸指示からスクリーンショットを自動撮影
