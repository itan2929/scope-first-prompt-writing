# Scope-First Prompt Writing

実装プロンプトや技術仕様を、対象範囲がぶれない形へ整理するCodex Skillです。

リリース全体の背景と今回の成果物を分け、今回実装する機能、境界、検証条件を短く明確にします。通常の否定表現は、実装とテストで確認できる肯定的な条件へ置き換えます。

## 構成

- `SKILL.md`: Skill本体の指示
- `references/negative-to-positive.md`: 境界表現の変換例と確認項目
- `agents/openai.yaml`: Codex UI向けメタデータ

## 導入

Codexから導入する場合:

```bash
npx skills add https://github.com/itan2929/scope-first-prompt-writing --global --yes --copy
```

手動で配置する場合は、リポジトリ直下のファイルをCodexのSkillディレクトリへコピーします。

```text
${CODEX_HOME:-$HOME/.codex}/skills/scope-first-prompt-writing/
```

## 使い方

複数のロードマップ要素を含む実装プロンプトの整理や、既存プロンプトの精査を依頼するときに使います。明示的に指定する場合は、プロンプトへ次を付けます。

```text
$scope-first-prompt-writingを使って、今回の実装範囲を整理してください。
```

## 検証

```bash
python3 /Users/katada/.codex/skills/.system/skill-creator/scripts/quick_validate.py .
```

## ライセンス

MIT Licenseです。詳細は[LICENSE](LICENSE)を参照してください。
