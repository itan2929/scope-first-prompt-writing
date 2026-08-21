---
name: scope-first-prompt-writing
description: Draft or revise implementation prompts and technical specs when several roadmap concerns are mixed together. Apply concise technical-writing principles, separate one deliverable from version-wide context, and rewrite ordinary negative constraints as positive boundaries.
---

# Scope-First Prompt Writing

Use this skill for implementation prompts, Beta specifications, technical briefs, and handoffs that feel too broad, repetitive, or dominated by negative wording.

## Workflow

1. Classify each request as the current deliverable, version context, existing invariant, later candidate, or delivery record.
2. State one current deliverable in the opening section.
3. Put only the behavior, data, API, UI, and tests needed for that deliverable into the main requirements.
4. Keep version-wide themes as a short context paragraph. Move later candidates to a short boundary note or a separate document.
5. Rewrite ordinary scope restrictions as positive, testable boundaries.
6. Keep security, privacy, tenant isolation, destructive-operation, and compatibility guardrails explicit.

Do not turn a release theme into a feature bundle. “AI summaries, analytics, UI/UX, and handoff” can be the release context while a Beta implements only AI summaries.

## Technical-Writing Baseline

Use one name for one concept. Prefer short, familiar words, active verbs, concrete routes and fields, and one testable instruction per bullet. Remove filler, marketing language, duplicate requirements, and broad introductions. Keep detail when it changes implementation or verification.

Use this compact document shape when it fits:

1. 位置づけ
2. 今回の実装対象
3. 前提と現状
4. 画面・API・データの振る舞い
5. セキュリティと既存データの境界
6. 検証
7. 未確定事項
8. 引き継ぎと完了条件

## Positive Boundaries

Prefer these forms for ordinary scope and behavior:

- `今回の対象はXに限る`
- `Xを正とする`
- `Xの権限だけに公開する`
- `Xを保持したままYを追加する`
- `GETは保存済みデータを返し、POSTだけが外部処理を開始する`
- `画面変更はXの操作と表示に限定する`

| Avoid as the main wording | Prefer |
| --- | --- |
| ページを開いたときにAPIを呼び出さない | `GET`は保存済み結果を返し、生成は明示操作のPOSTで開始する |
| 企業画面へ公開しない | 閲覧権限を開発者管理者に限定する |
| UI全体を改修しない | 画面変更を対象機能の操作と表示に限る |
| 既存候補を消さない | 既存候補を保持した下書きへ追加・編集を適用する |
| 自動生成を行わない | 生成開始を管理者の明示操作を起点にする |

Do not delete a negative sentence when it expresses a real security or integrity control. Prefer a positive server-side boundary, but keep the prohibited outcome and its test explicit.

## Preserve Decisions

Do not use editing style to change a product decision. Record genuinely undecided policies under `未確定事項` with the decision needed and its implementation impact. Keep “later in the roadmap” separate from “must never happen.”

When a requirement crosses layers, align the UI action, API authorization, server source of truth, database behavior, privacy boundary, and focused test. State each rule once and reference it instead of repeating it in every section.

## File Placement

Respect the user’s requested destination. If no destination is specified for a prompt, ask before creating a repository file or personal-vault note. Do not infer that a prompt belongs in the active application repository. When a personal vault is named, keep the note there and do not duplicate it into the application repository unless explicitly requested.

## Final Check

- The opening names one current deliverable.
- Version-wide themes are context, not hidden extra implementation work.
- Main requirements are implementable and testable.
- Ordinary scope restrictions use positive boundaries.
- Security and data-integrity guardrails remain explicit.
- Later work and unresolved decisions are separate from acceptance criteria.
- The prompt does not repeat one rule under different names.
- The requested destination is respected.

Read [references/negative-to-positive.md](references/negative-to-positive.md) for additional wording examples when the prompt needs that review.
