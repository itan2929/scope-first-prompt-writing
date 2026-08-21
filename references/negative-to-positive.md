# Negative-to-Positive Review Guide

Use this reference when a prompt repeats `〜しない`, `〜行わない`, `禁止`, or `対象外`.

## Rewrite Table

| Negative wording | Positive boundary |
| --- | --- |
| Beta-01では分析画面を作らない | Beta-01は回答まとめのAI生成操作と表示を対象にする |
| 生成機能以外は実装しない | 実装対象は生成API、保存済み結果、状態表示、画面操作である |
| ページを開いただけで生成しない | 生成開始は管理者の明示操作を起点にする |
| 既存フォームを変更しない | 発行済みフォームは発行時のスナップショットを使い続ける |
| 既存候補を削除しない | 追加・編集は候補単位で適用し、既存候補の同一性を保持する |
| 他企業の回答を混ぜない | 企業をサーバー側で確定し、集計をその企業の範囲で実行する |
| APIキーをフロントへ出さない | APIキーをサーバー専用設定で管理し、ブラウザへ渡さない |

## Review Rule

First state the behavior that exists. Then state the actor, source of truth, and affected boundary. Put a prohibition in the requirement only when the prohibited outcome is itself a security, privacy, integrity, or compatibility control. Keep the corresponding test explicit.
