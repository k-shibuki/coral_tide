# Markdown Style Guide

**このドキュメントは、プロジェクトにおける Markdown ファイルの意味的構造や内容に関する補足的なガイドラインを提供します。**
**フォーマットに関する主たるルールは `.markdownlint-cli2.jsonc` ファイルで定義されており、そのルールに基づく Lint プロセス (通常は `03_executor.mdc` の Stage 3-d) によってフォーマットは自動的に修正されます。**

このガイドは、Lint ルールだけでは表現しきれない意図や、執筆時の推奨事項を示します。

---

## 書式ルール (補足)

以下は `.markdownlint-cli2.jsonc` で定義されたルールの一部と、それに関する補足的な推奨事項です。

### リスト

- **リストマーカーにはハイフン (`-`) を使用します。** (`.markdownlint-cli2.jsonc` の `MD004: { "style": "dash" }` 設定に対応)
- ネストされたリスト項目は、親リスト項目のマーカー (`-`) の開始位置に合わせて **スペース2つ** でインデントします。 (`.markdownlint-cli2.jsonc` の `MD007: { "indent": 2 }` 設定に対応)

  ```markdown
  - Level 1
    - Level 2
      - Level 3
  ```

### 見出し

- ドキュメントの構成に応じて適切なレベルを使用してください。
- 見出しレベル1 (`#`) は、ドキュメント全体のタイトルとして原則1回のみ使用することを推奨します。ただし、Lint ルール (`.markdownlint-cli2.jsonc` の `MD041: false`) では、ファイル冒頭にレベル1見出しがあることは必須としていません。
- 見出しの前後に空行を1行入れてください (markdownlint: MD022)。

### コードブロック

- コードブロックには言語指定を必ず行ってください (例: ```typescript)。(`.markdownlint-cli2.jsonc` の `MD040: true` 設定に対応)

### 文字数制限

- 1行の文字数制限はありません (markdownlint: MD013=false)。ただし、可読性の観点から、長すぎる行は適宜改行することを推奨します。

### インラインHTML

- 原則としてMarkdown構文を使用してください。
- 例外的に許可されるHTML要素は `<details>`, `<summary>`, `<br>` です (`.markdownlint-cli2.jsonc` の `MD033` 設定に対応)。

## Lintingルールセット (参考情報)

**フォーマットを定義・修正する主たる Lint ルールは、プロジェクトルートの `.markdownlint-cli2.jsonc` ファイルです。常にそちらを参照してください。**
以下は、参考情報としてそのファイルから抜粋した一部のルール設定とその意図です。

- `default: true`: デフォルトルールセットを有効化。
- `MD013: false`: 行の長さ制限なし (可読性のため適宜改行を推奨)。
- `MD004: { "style": "dash" }`: 箇条書きリストのマーカーとしてハイフン (`-`) を使用。
- `MD007: { "indent": 2 }`: ネストされたリストのインデントはスペース2つ。
- `MD033: allowed_elements: ["details", "summary", "br"]`: 特定のHTML要素 (`<details>`, `<summary>`, `<br>`) の使用を許可。
- `MD041: false`: ファイル先頭の見出しレベル1は必須としません (`.markdownlint-cli2.jsonc` で設定)。
- `MD040: true`: コードブロックの言語指定を必須とします (`.markdownlint-cli2.jsonc` で設定)。
