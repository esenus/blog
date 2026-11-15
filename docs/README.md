# Documentation

このディレクトリには、`blog` の目的、設計、コンテンツ、
実装方針に関するDocumentationを収録します。

## Documents

| Document | Purpose |
| --- | --- |
| [Concept](concept.md) | `blog` の目的と役割 |
| [Design](design.md) | サイト構造とInteraction |
| [Content](content.md) | Content Sectionと掲載方針 |
| [Wireframes](wireframes.md) | Page LayoutとResponsive Structure |
| [Architecture](architecture.md) | Implementation Structureと責務の境界 |

## Scope

このDocumentationでは、`blog` 自体の目的、設計、コンテンツ、
実装方針を扱います。

esenus全体のConceptや、Loom、Nestなど他のProjectの詳細仕様は、
それぞれのProjectが管理するDocumentationを参照します。

`blog` はLoomを利用して構築・公開するWebサイトです。
Loom自体の仕組みや共通仕様は、Loom側のDocumentationで定義します。

## Documentation Approach

Documentationは、設計判断と実装を継続するために必要な範囲で整備します。

標準規格やArchitecture手法は参考にしますが、
形式への準拠そのものを目的としません。

参考とする考え方：

- **arc42** — Architecture Documentation
- **ISO/IEC/IEEE 29148** — Requirements Engineering
- **C4 Model** — Software Architecture Diagrams
- **ADR** — Architecture Decision Records

## Writing Rules

- 各Documentの目的と責務を明確にする。
- 短く具体的に記述する。
- Architecture用語や固有のNamingは、原則として英語表記を維持する。
- 同じ説明を複数のDocumentに重複して記載しない。
- 決定事項、提案、未決事項を区別する。
- 現在の実装と、今後の構想を区別する。
- 実装から読み取れる事実と、設計として決定した事項を混同しない。
- 将来の可能性だけを理由に、仕様や仕組みを増やさない。
- 実装や設計に変更があった場合は、関連するDocumentを更新する。