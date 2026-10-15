# Architecture

## Overview

`muse` は、HTML、CSS、JavaScriptを中心としたWebサイトとして試作されています。提供されたソースでは、画面構造をHTML、表示とResponsive LayoutをCSS、NavigationやPanelなどの操作をJavaScriptで実装しています。

現時点では、Central DatabaseやBackendを前提としません。

## Current Structure

- **HTML** — Header、Navigation、Hero、各Section、Sticky Action、Panel、Footerなどの文書構造を定義する。
- **CSS** — 色、Typography、Layout、Responsive Behavior、Transitionを定義する。
- **JavaScript** — Content Gridの試作用生成、現在位置に応じた表示状態の更新、Navigation、Panelの開閉を扱う。

提供されたソースのGridは、`data-grid-count` と `data-grid-prefix` を使って仮のItemを生成しています。これは表示確認用の実装であり、実際のContent管理方式を確定するものではありません。

## Publishing

`muse` は公開Webサイトとして提供します。Build方法、Repository構成、公開先、ContentをHTMLへ反映する方法の詳細は、この試作だけでは確定していないため、必要になった段階で別途定義します。

## Boundaries

- `muse` は活動の様子を外部に見せる役割を担う。
- Contentの管理機構やBackendを、必要性がない段階で追加しない。
- `www` など他のAreaと、単一のApplicationやNavigationに統合しない。
- 共通の仕組みは、実際の重複や必要性が確認されてから検討する。
- 試作コードの構造と、確定した仕様を混同しない。



## Development Approach

まずは現在のサイト構成とInteractionを整理し、実際のContentを載せるために必要な変更を明確にします。抽象的なContent Engineや共通Backendなどは、具体的な課題が生じるまで導入しません。