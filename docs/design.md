# Design

## Direction

`muse` は、活動の様子が見える場所として、Contentを中心に構成します。情報を整理しながらも、活動を固い構造に押し込みません。

- **Clear** — 構造が理解しやすい
- **Flexible** — 変化や追加に対応できる
- **Playful** — 少し遊べる
- **Quiet** — Contentを中心に見せる
- **Imperfect** — 途中のものも自然に置ける

整っているけれど、固すぎない。シンプルだけれど、少し遊べる。

## Site Structure

### HOME

サイトの入口。活動の雰囲気を伝え、最近の更新を表示します。

### PLAY

試していること、実験、プロトタイプ、未完成のアイデアなどを扱います。

### MAKE

Webサイト、Software、Hardware、Designなど、実際につくったものを扱います。

### NOTE

制作や活動の中で生まれた考え、発見、技術的なメモ、記録などを扱います。

### ARCHIVE

過去の活動や、終了・停止したものを含む記録を残します。過去のものを、現在の活動から切り離して消すのではなく、時間の中に位置づけます。

### KNOCK

SNSなど、esenusへ連絡するための外部リンクをまとめます。

### BEHIND

寄り道、ボツ案、ラフなメモ、裏話など、形式を整えすぎない断片を扱います。

## Interaction

想定するUIは、固定されたLogo、画面位置に応じて変化するNavigation、最近の更新、SectionごとのContent Grid、KNOCKとBEHINDを開くSticky Actionです。

- Desktopでは、Homeと各SectionでNavigationの配置を切り替える。
- Mobileでは、画面下部にNavigationを配置する。
- Sticky ActionはPanelとして開閉できる。
- `Escape` キーで開いているPanelを閉じられる。
- 動きを減らす設定が有効な場合は、アニメーションを抑える。

これらは、提供されたHTML試作に見られる構成を整理したものです。画面寸法や細かなAnimation値は、このDocumentでは固定しません。

## Content Presentation

Contentは、完成度や規模だけで選別しません。必要に応じて、タイトル、短い説明、日付、画像などを使って、何が行われているかを把握できるようにします。

具体的なContent Schema、更新方法、表示件数などは、必要性が明確になってから定義します。