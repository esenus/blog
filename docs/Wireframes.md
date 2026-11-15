# Wireframes

## Purpose

このDocumentでは、`blog` の各Pageにおける要素の構成、情報の優先順位、Navigation、Responsive Behaviorを定義する。

サイト全体の設計方針は `design.md`、Contentの掲載方針と分類方法は `content.md` を参照する。

## Conventions

- Wireframeは、ContentとUIの構造を伝えるためのものである。
- 色、Typography、AnimationなどのVisual Designは、必要な場合を除き詳細に定義しない。
- ASCII Diagramは構造を示す概念図とし、実際の寸法や配置を保証するものではない。
- 現在の実装と今後の構想を区別する。
- 実装が変更された場合は、関連するWireframeも更新する。

## 1. HOME

### Purpose

`blog` の雰囲気を伝え、注目するContentや各Sectionへの導線を提供する。

### Structure

```
┌──────────────────────────────────┐
│ Header / Logo                    │
│ Primary Navigation               │
├──────────────────────────────────┤
│                                  │
│ Hero                             │
│ PLAY GROUND.                     │
│                                  │
├──────────────────────────────────┤
│ TOPICS                           │
│ Featured Content                 │
├──────────────────────────────────┤
│ NOTE                             │
│ Latest Content (up to 6 items)   │
│ Link to NOTE                     │
├──────────────────────────────────┤
│ PLAY / MAKE / THEN               │
│ Section Entry Points             │
├──────────────────────────────────┤
│ Footer                           │
└──────────────────────────────────┘
```

この図はHOMEの情報構造を示す概念図であり、実際の表示順や配置は最新の実装を基準とする。

### Content Priority

1. サイトのIdentity
2. 注目するContent
3. 最近の活動記録
4. 各Sectionへの導線

TOPICSとNOTEの最新一覧は、それぞれ異なる目的を持つ。

TOPICSは注目するContentを紹介し、NOTEは新しい記録を継続して見せる。

## 2. NOTE



### Purpose

公開中の記事を新しい順に一覧表示し、個々のContentへ移動できるようにする。

NOTEは記事を時系列でまとめるViewであり、記事の所属Sectionとは独立している。

### Desktop Structure

```
┌──────────────────────────────────┐
│ Header / Navigation              │
├──────────────────────────────────┤
│ Section Heading                  │
│ NOTE                             │
├──────────────────────────────────┤
│ Content List / Grid              │
│                                  │
│ [Content] [Content]              │
│ [Content] [Content]              │
│ [Content] [Content]              │
│                                  │
├──────────────────────────────────┤
│ Pagination                       │
│ ← PREV  01  02  03  NEXT →       │
│                                  │
│ MORE NOTES → (if 3+ pages)       │
├──────────────────────────────────┤
│ Footer                           │
└──────────────────────────────────┘
```



#### Desktop Behavior

- 1ページあたり6件を表示する。
- 複数ページがある場合はPaginationを表示する。
- 現在のページを識別できるようにする。
- 前後のページへ移動できるようにする。
- 3ページ以上ある場合は、一覧の末尾に `MORE NOTES →` を表示する。
- `MORE NOTES →` はNOTEのArchive Viewへ誘導する。



### Mobile Structure

```
┌──────────────────────────────────┐
│ Header / Logo                    │
│                                  │
│ SUB Navigation                   │
│ HOME NOTE PLAY MAKE THEN         │
│                                  │
├──────────────────────────────────┤
│ Section Heading                  │
│ NOTE                             │
├──────────────────────────────────┤
│                                  │
│ Content List                     │
│                                  │
│ [Content]                        │
│ [Content]                        │
│ [Content]                        │
│ [Content]                        │
│ ...                              │
│                                  │
│ All Published Notes              │
│                                  │
├──────────────────────────────────┤
│ MORE NOTES →                     │
├──────────────────────────────────┤
│ Footer                           │
└──────────────────────────────────┘
```



#### Mobile Behavior

- Paginationは表示しない。
- 公開中のNOTEをすべて一覧表示する。
- 現在の実装では18件を表示する。
- 一覧の末尾に `MORE NOTES →` を配置する。
- ページ番号や前後移動の操作UIは設けない。

DesktopとMobileでは、同じContentを異なる一覧表示方法で提供する。

## 3. PLAY



### Purpose

進行中のProject、実験、探索、プロトタイプなどを紹介する。

### Structure

```
┌──────────────────────────────────┐
│ Header / Navigation              │
├──────────────────────────────────┤
│ Section Heading                  │
│ PLAY                             │
├──────────────────────────────────┤
│ Projects / Exploration           │
│                                  │
│ [Item]  [Item]                   │
│ [Item]  [Item]                   │
│                                  │
├──────────────────────────────────┤
│ Footer                           │
└──────────────────────────────────┘
```



### Content Behavior

- 進行中のProjectや試みを一覧表示する。
- Contentの状態や進行状況を必要に応じて表示できる。
- Collectionを設定したContentは、必要に応じて関連するまとまりを識別できる。
- Collectionを設定していないContentも同じSection内に掲載できる。

Collectionの一覧表示やFilter UIは、必要性が明確になるまで必須としない。

## 4. MAKE



### Purpose

制作物や、実際につくったもの、制作過程や実験を紹介する。

### Structure

```
┌──────────────────────────────────┐
│ Header / Navigation              │
├──────────────────────────────────┤
│ Section Heading                  │
│ MAKE                             │
├──────────────────────────────────┤
│ Things Made                      │
│                                  │
│ [Item]  [Item]                   │
│ [Item]  [Item]                   │
│                                  │
├──────────────────────────────────┤
│ Footer                           │
└──────────────────────────────────┘
```



### Content Behavior

画像の有無やContentの形に応じて、一覧内の表示方法を調整できる構造とする。

Software、Hardware、Web、Design、料理、工作など、分野を限定せずに掲載できるようにする。

Collectionを設定していないContentも掲載できる。

## 5. THEN



### Purpose

日々の記録や、過去の活動、出来事、場所、思考などをたどれるようにする。

日記やつぶやきのような短いContent、まだ分類されていない記録も扱う。

### Structure

```
┌──────────────────────────────────┐
│ Header / Navigation              │
├──────────────────────────────────┤
│ Section Heading                  │
│ THEN                             │
├──────────────────────────────────┤
│ Personal Records / Past Content │
│                                  │
│ [Item]  [Item]                   │
│ [Item]  [Item]                   │
│                                  │
├──────────────────────────────────┤
│ Footer                           │
└──────────────────────────────────┘
```



### Content Behavior

- 過去の活動や作品、出来事などを掲載する。
- 日記、つぶやき、短いメモなども掲載できる。
- Collectionを設定していないContentも掲載できる。
- `Unsorted` は、分類先が決まっていないContentを置くためのCollectionとして扱う。
- UnsortedのContentも、他のContentと同様に一覧から閲覧できる。

Collectionの一覧表示やFilter UIは、必要性が明確になるまで必須としない。

## 6. Content Detail



### Purpose

個々のContentを読み、関連する情報へ移動できるようにする。

### Structure

```
┌──────────────────────────────────┐
│ Header / Navigation              │
├──────────────────────────────────┤
│ Section / Breadcrumb (if needed) │
├──────────────────────────────────┤
│ Title                            │
│ Date / Metadata (if needed)      │
├──────────────────────────────────┤
│                                  │
│ Main Content                     │
│ Text / Images / Media            │
│                                  │
├──────────────────────────────────┤
│ Related Content (if applicable)  │
│ Back to Blog / Section           │
├──────────────────────────────────┤
│ Footer                           │
└──────────────────────────────────┘
```

個別Pageの具体的な構造は、LoomにおけるContentの公開方式と実際のContent形式が確定した段階で更新する。

## 7. Shared UI

共通UIについては、次の項目を確認する。

- HeaderとLogo
- Primary Navigation
- Mobile SUB Navigation
- Sticky UIや補助Panel（実装に存在する場合）
- Footer
- Linkと外部Linkの表示
- Hover、Focus、Activeなどの状態
- PanelのOpen / Close
- Keyboard Interaction



### Mobile SUB Navigation

Mobileでは、SUB Navigationを画面上部に固定して表示する。

- HOME / NOTE / PLAY / MAKE / THENへの移動を提供する。
- 現在のSectionやPageの状態を反映する。
- Navigationの背後には、上部から下方向へ広がるBlurを設ける。
- BlurはNavigationと、その周辺に配置される操作要素の背後まで覆う。
- Contentの閲覧を妨げない範囲で、Navigationの視認性を確保する。



## 8. Responsive Layout



### Desktop

- HeaderとNavigationを視認しやすく配置する。
- Contentの一覧性と余白を維持する。
- 画面幅を活用しながら、読みやすさを優先する。
- NOTEは6件単位で表示し、必要に応じてPaginationを使用する。



### Mobile

- SUB Navigationから主要Sectionへアクセスできるようにする。
- SUB Navigationは画面上部に固定する。
- 上部のBlurによってNavigationと操作要素の視認性を確保する。
- Content Gridを画面幅に応じて再配置する。
- NOTEはページングせず、公開中のContentをすべて表示する。
- NOTEの一覧末尾に `MORE NOTES →` を配置する。
- Text、Image、Interactive Elementが画面からはみ出さないようにする。
- Desktop固有の配置や操作が閲覧・操作を妨げないようにする。

Breakpoint、列数、具体的な寸法は、実装と検証に基づいて定義する。

## Open Questions

- HOMEの各Sectionの最終的な表示順
- TOPICSの具体的なLayoutと表示件数
- NOTEの一覧とContent Detailの共通仕様
- Desktop / MobileでのNavigationの切替条件
- Sticky UIや補助Panelの最終的な仕様
- 画像を含むContentの表示パターン
- NOTEのArchive Viewの具体的な構成
- Collectionを一覧上でどのように表示するか

