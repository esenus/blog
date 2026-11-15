# Design

## Design Direction

`blog` は、活動の様子が見える場所として、Contentを中心に構成する。

情報を整理しながらも、活動を固い構造に押し込まない。

- **Clear** — 構造が理解しやすい
- **Flexible** — 変化や追加に対応できる
- **Playful** — 少し遊べる
- **Quiet** — Contentを中心に見せる
- **Imperfect** — 途中のものも自然に置ける

整っているけれど、固すぎない。

シンプルだけれど、少し遊べる。

## Identity

- Project name: `blog`
- Website: `https://blog.esenus.com/`
- Tagline: `PLAY GROUND.`
- Copyright: `© 2026 ESENUS BLOG`

## Information Architecture

Primary Navigation:

`HOME → NOTE → PLAY → MAKE → THEN`

### HOME

サイト全体の入口。

`blog` の雰囲気を伝え、注目するContentや最近の活動へ導く。

### NOTE

文章を中心とするContentを時系列で一覧表示する。

日々の記録、考えたこと、発見、技術的なメモなどを掲載する。

NOTEは独立したContentの分類ではなく、公開中の記事を新しい順にまとめて閲覧するためのViewとして扱う。

### PLAY

進行中のProjectや、試していること、探索、実験、プロトタイプなどを扱う。

完成や成果だけでなく、活動が進んでいく様子を見せる。

関連するサービスやProjectの紹介も含める。

### MAKE

実際につくることや、制作を通して生まれるものを扱う。

Software、Hardware、Web、Design、料理、工作など、分野を限定しない。

完成品だけでなく、試作や制作過程、実験も含める。

### THEN

日々の記録や、過去の活動、出来事、場所、思考などを扱う。

日記やつぶやきのような短い記録、まだ分類されていないContentも自然に置ける場所とする。

過去の経験や記録を、現在の活動から切り離さず、時間の積み重ねとしてたどれるようにする。

## Navigation

Primary Navigationは、すべての主要Sectionにアクセスするための共通導線とする。

Navigationの表示位置や配置は、画面幅とPageの状態に応じて変化してよい。ただし、Sectionの意味と移動先は一貫させる。

DesktopとMobileでは、画面構成に応じてNavigationの位置や補助UIの配置を変える。

Mobileでは、画面上部に固定されるSUB Navigationを使用する。SUBの背景には上部から下方向へ広がるBlurを設け、Navigationや関連する操作要素の背後まで視認性を確保する。

## Interaction

Interactionは、Contentの閲覧を妨げず、サイトの個性を伝えるために使用する。

- Navigationから各Sectionへ移動できる。
- Contentから詳細ページや関連する外部サイトへ移動できる。
- Panelなどの補助UIは、開閉状態を明確にする。
- キーボードから主要な操作を行えるようにする。
- `Escape` によるPanelの終了をサポートする場合、対象となるUIを明確にする。
- `prefers-reduced-motion` が有効な場合、不要なAnimationを抑える。

具体的な配置、表示状態、Responsive Behaviorは `wireframes.md` と実装を参照する。

## Content Presentation

Contentは、タイトル、短い説明、日付、画像などを用いて、内容や活動の様子を把握できるようにする。

すべてのContentに同一の表示要素を必須とするのではなく、内容に応じて必要な情報を選択する。

一覧表示では、Contentの種類やSectionに応じて表示形式を調整する。

Section、Collection、Tagsによる分類と掲載基準は `content.md` で定義する。

## Responsive Design

DesktopとMobileの双方で、Contentの読みやすさとNavigationの使いやすさを維持する。

画面幅に応じて配置や表示方法を変更しても、主要な情報と操作へのアクセスを失わないことを基本とする。

同じContentでも、画面幅に応じて一覧の表示件数や操作方法を変更してよい。

NOTEの一覧表示は、DesktopとMobileで次のように扱う。

- Desktop：6件単位で表示し、必要に応じてPaginationを使用する。
- Mobile：ページングを行わず、公開中のNOTEをまとめて表示する。

具体的なBreakpointや寸法は、実装上の必要性が確認できた段階で定義する。

## Accessibility

- Semantic HTMLを基本とする。
- キーボード操作とFocus状態を考慮する。
- 画像には内容に応じた代替テキストを設定する。
- 色だけに依存して情報を伝えない。
- Animationを抑制するユーザー設定を尊重する。
- NavigationやPaginationなどの操作要素は、状態や目的を識別できるようにする。