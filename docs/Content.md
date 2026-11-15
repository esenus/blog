# Content

## Purpose

このDocumentでは、`blog` に掲載するContentの種類、各Sectionの役割、分類方法、掲載時の判断基準を定義する。

画面上の配置や表示方法は `design.md` と `wireframes.md` を参照する。

## Content Principles

- 完成品だけでなく、活動の途中経過も扱う。
- Contentの規模や完成度だけで掲載可否を決めない。
- Contentの種類を必要以上に細分化しない。
- 複数のSectionに関係するContentは、主な目的に基づいて配置する。
- Collectionへの分類は必須としない。
- 分類先が決まっていないContentも、そのまま掲載できるようにする。
- 過去のContentも、必要に応じて継続して閲覧できるようにする。
- Contentは、活動の変化に合わせて更新・追加できるものとする。

## Information Model

`blog` では、Contentの分類と閲覧方法を区別する。

### Section

Contentが属する主な活動領域。

- `PLAY` — 進行中のProject、探索、試み
- `MAKE` — 制作、試作、実験、つくったもの
- `THEN` — 日々の記録、過去の活動、出来事、思考

各Contentは、原則として主となるSectionをひとつ持つ。

### Collection

Section内のContentを、必要に応じてまとめるための任意の分類。

CollectionはContentの掲載に必須ではない。分類する必要がないものや、分類先がまだ決まっていないものは、Collectionを設定せずに掲載できる。

CollectionはSectionごとに設ける。異なるSectionで同じ名前を使用しても、それぞれ独立した分類として扱う。

Collectionの例：

- PLAY：Projects、Web、Electronics
- MAKE：Development、Experiments、Tools、Web、Food、Electronics
- THEN：Unsorted、Works、Photographs、Old Website、Old Ideas

上記は現時点の候補であり、Contentの増加や運用に応じて追加・変更できる。

### Tags

SectionやCollectionを横断して、Content同士を関連付けるためのキーワード。

例：

- `web`
- `design`
- `experiments`
- `electronics`
- `records`
- `ideas`

TagsはContentのテーマや関連性を表すものであり、SectionやCollectionの代わりにはしない。

### View

Contentを特定の目的や順序でまとめて閲覧するための表示単位。

- `NOTE` — 公開中の記事を新しい順に表示するView
- `TOPICS` — 注目する記事やContentを選んで表示するView

NOTEはSectionとは別のViewとして扱う。記事はPLAY、MAKE、THENのいずれかに属しながら、NOTEにも表示される。

TOPICSはSectionやCollectionに属するContentを横断して選定できる。

## Sections

### PLAY

**Purpose:** Projects and exploration.

進行中のProjectや、新しいことを試している活動を扱う。

対象となるContent：

- 進行中のProject
- 新しい試みや探索
- 実験やプロトタイプ
- 進行中のアイデア
- 関連するサービスやProjectの紹介

完成や公開を前提とせず、活動の途中にあるものも扱う。

活動の経過や変化が見えることを重視する。

### MAKE

**Purpose:** Making and things made.

実際につくることや、制作を通して生まれたものを扱う。

対象となるContent：

- Software
- Hardware
- Webサイト
- Design
- 料理
- 工作やDIY
- 試作や制作過程
- その他、実際につくったものや試したこと

分野や制作規模を限定しない。

完成品だけでなく、制作の途中で得られた発見や試行錯誤も扱う。

### THEN

**Purpose:** Personal records and the past.

日々の記録や、過去の活動、出来事、場所、思考などを扱う。

対象となるContent：

- 日記や日々の出来事
- つぶやきや短いメモ
- 断片的な思考や気づき
- 過去の活動やProject
- 過去の作品
- 旅行や訪れた場所の記録
- 写真や過去のWebサイト
- 現在の活動から時間的に離れた記録

THENは、完成した記録や整理済みの情報だけを扱うSectionではない。

日々の小さな記録や、まだ分類されていないContentも自然に置ける場所とする。

#### Unsorted

`Unsorted` は、THEN内で分類先が決まっていないContentを置くためのCollectionとする。

対象となるContent：

- 日記
- つぶやき
- 短いメモ
- 断片的な思考
- 日々の小さな発見
- まだ他のCollectionに分類していない記録

Unsortedは「分類できないもの」ではなく、「まだ分類していないもの」を受け入れるための場所とする。

後から必要に応じて別のCollectionへ移動できる。Unsortedのまま残すこともできる。

## NOTE

**Purpose:** Thoughts and records.

NOTEは、公開中の記事を時系列で閲覧するための一覧Viewとする。

対象となるContent：

- 日々の記録
- 考えたことや発見
- 技術的なメモ
- 活動の記録
- その他、文章を中心とするContent

NOTEには、PLAY、MAKE、THENなどに属する公開中の記事を含め、新しい順に表示する。

NOTE自体はSectionではなく、記事の所属先を変更するものでもない。

### Display Behavior

- Desktopでは、1ページあたり6件を表示する。
- Desktopでは、複数ページに分けて閲覧できるPaginationを設ける。
- 3ページ以上になる場合は、一覧の末尾に `MORE NOTES →` を表示し、NOTEのArchive Viewへ誘導する。
- MobileではPaginationを使用せず、公開中のNOTEをすべて表示する。
- Mobileでは、全件表示した一覧の末尾に `MORE NOTES →` を表示する。

現在の実装では、MobileのNOTEは18件を表示する。件数が増減した場合も、Mobileではページングを設けず全件表示する方針とする。

## HOME Content

HOMEは、サイトの入口としてContentの存在を伝え、各Sectionへ移動するきっかけをつくる。

注目するContentを紹介する領域として `TOPICS` を設ける。

TOPICSは、単なる新着順とは限らず、特に見せたいContentや活動を取り上げるためのViewとする。

NOTEの最新Contentを表示する領域とは役割を分ける。

NOTEの最新一覧は最大6件を基本とし、過去のContentへはNOTEの一覧Viewからアクセスできるようにする。

掲載件数、表示順、選定・更新方法は、実装と運用に合わせて確定する。

## Content Placement

複数のSectionに関係するContentは、そのContentを最もよく表す目的を基準に配置する。

- 進行中のProjectや探索が中心なら PLAY
- つくること、制作、試作、実験が中心なら MAKE
- 日々の記録や過去の活動、出来事、思考が中心なら THEN

文章形式のContentは、属するSectionにかかわらずNOTEの一覧Viewにも表示される。

注目するContentは、必要に応じてTOPICSにも掲載できる。

Collectionは必要な場合にのみ設定する。分類先が明確でない場合は、無理に分類しない。

必要に応じて、本文や関連リンクから他のContentへ接続する。

## Content Lifecycle

Contentは、活動の進行や時間の経過に合わせて更新されることがある。

公開中のContentが過去の記録になった場合も、自動的に削除することを前提としない。

SectionやCollectionの変更、公開状態、更新方法などは、実際のPublishing Workflowに合わせて定義する。

## Open Questions

- TOPICSの選定・更新方法
- ContentのURLとPermalinkの方針
- Content間の関連付け方法
- Tagsの運用ルール
- Collectionの追加・変更方法
- Contentの公開・非公開・下書きの扱い
- Sectionを変更する場合の運用方法
- NOTEのArchive Viewの具体的な構成