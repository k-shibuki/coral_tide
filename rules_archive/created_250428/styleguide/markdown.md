# Markdown スタイルガイド

このプロジェクトにおけるMarkdownファイルの書き方ガイドラインです。
`@coding.mdc` から参照され、静的な書式ルールを定義します。
Lintingルールは `.markdownlint.jsonc` で定義され、その実行は `@linting.mdc` で指示されます。

## 書式ルール

### リスト

- **リストマーカーにはハイフン (`-`) を使用します。**
- ネストされたリスト項目は、親リスト項目のマーカー (`-`) の開始位置に合わせて **スペース2つ** でインデントします。

  ```markdown
  - Level 1
    - Level 2
      - Level 3
  ```

### 見出し

- ドキュメントの構成に応じて適切なレベルを使用してください。
- 見出しレベル1 (`#`) はファイル名と重複するため、通常は使用しません。
- 見出しの前後に空行を1行入れてください (markdownlint: MD022)。

### コードブロック

- コードブロックには言語指定を必ず行ってください (例: ```typescript)。(markdownlint: MD040)

### 文字数制限

- 1行の文字数制限はありません (markdownlint: MD013=false)。ただし、可読性の観点から、長すぎる行は適宜改行することを推奨します。

### インラインHTML

- 原則としてMarkdown構文を使用してください。
- 例外的に許可されるHTML要素は `<details>`, `<summary>`, `<br>` です (markdownlint: MD033)。

## Lintingルールセット

詳細なルールは `.markdownlint.jsonc` を参照してください。主な設定は以下の通りです。

- `default: true`: デフォルトルールセットを有効化。
- `MD013: false`: 行の長さ制限なし。
- `MD033: allowed_elements: ["details", "summary", "br"]`: 特定のHTML要素を許可。
- `MD041: false`: ファイル先頭の見出しレベル1を必須としない。
