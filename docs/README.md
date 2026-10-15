# Documentation

このディレクトリには、`muse` の目的、設計、実装方針に関するDocumentationを収録します。

## Documents


| Document                        | 目的                |
| ------------------------------- | ----------------- |
| [Concept](concept.md)           | `muse` が担う役割を定義する |
| [Design](design.md)             | サイトの構成と表示方針を定義する  |
| [Architecture](architecture.md) | 実装の構成と責務の境界を定義する  |


## Scope

このDocumentationでは、`muse` 自体の目的、設計、実装方針を扱います。

esenus全体のConceptや、Loom、Nestなど他のProjectの詳細仕様はここでは定義しません。それぞれのProjectが管理するDocumentationを参照します。

画面や機能の詳細は、必要性が明確になった段階で追加します。

## Documentation Approach

標準規格やArchitecture手法は参考にしますが、準拠そのものを目的としません。

必要な考え方を軽量に取り入れ、`muse` の規模と実際の課題に合わせてDocumentationを整備します。

参考とする考え方：

- **arc42** — Architecture Documentation
- **ISO/IEC/IEEE 29148** — Requirements Engineering
- **C4 Model** — Software Architecture Diagrams
- **ADR** — Architecture Decision Records

厳密なテンプレートへの適合は求めません。

## Writing Rules

- 各Documentの目的を明確にする。
- 短く具体的に記述する。
- Architecture用語や固有のNamingは、原則として英語表記を維持する。
- 同じ説明を複数のDocumentに重複して記載しない。
- 現在の実装と、今後の構想を区別する。
- 将来の可能性だけを理由に、仕様や仕組みを増やさない。
- 実装から読み取れる事項と、設計として決定した事項を混同しない。

