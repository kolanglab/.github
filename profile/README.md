# kolanglab

**言語処理系（コンパイラ・インタプリタ・GC など）を題材にした技術書・教材**を公開しています。
「作って理解する」ことを目標に、手を動かしながら読める本を揃えています。

## 📚 本・教材

| 本 | 内容 | 読む |
|---|---|---|
| **言語処理系を作りたい人のためのC言語入門** | 処理系を書くために必要な C を、目的から逆算して学ぶ | [📖 公開版](https://kolanglab.github.io/book_clang_intro/) ／ [repo](https://github.com/kolanglab/book_clang_intro) |
| **構文解析入門** | AST の作り方を、簡単な文法からパーサージェネレータ・理論・最先端まで網羅する入門 | [📖 公開版](https://kolanglab.github.io/book_parser_intro/) ／ [repo](https://github.com/kolanglab/book_parser_intro) |
| **言語処理系の意味解析入門** | AST に対する名前解決・型検査/推論・制御/データフロー解析・抽象解釈を紹介 | [📖 公開版](https://kolanglab.github.io/book_semantic_intro/) ／ [repo](https://github.com/kolanglab/book_semantic_intro) |
| **コード生成入門** | AST 取得後のコード生成を、IR・命令選択・レジスタ割り当て・最適化・JIT までコンパイラ視点で | [📖 公開版](https://kolanglab.github.io/book_code_gen/) ／ [repo](https://github.com/kolanglab/book_code_gen) |
| **精密 GC をインタプリタに実装する** | インタプリタに正確な（precise）GC を実装する | [📖 公開版](https://kolanglab.github.io/book_precise_gc/) ／ [repo](https://github.com/kolanglab/book_precise_gc) |
| **保守的GC入門** | 保守的 GC を libgc で作る方法と、その裏側の理論 | [📖 公開版](https://kolanglab.github.io/book_Conservative_GC/) ／ [repo](https://github.com/kolanglab/book_Conservative_GC) |
| **GC最前線** | GC 実装方式の研究と実装、2026年時点の最前線を詳説 | [📖 公開版](https://kolanglab.github.io/book_gc_details/) ／ [repo](https://github.com/kolanglab/book_gc_details) |

## 💬 フィードバック・質問

各本の **Issue** から、誤り・わかりにくい点・疑問をどうぞ。
公開ページでは本文を選択して「Report as issue」からも送れます。

寄せられた質問や指摘は、内容に応じて回答・本文修正に反映していきます。
受講者は **質問 → 議論 → 修正の提案・反映** までリポジトリ上で行えます。

## 🛠 ビルドについて

各本は [ligarb](https://github.com/ko1/ligarb) で Markdown から生成しています。
ローカルでのビルド手順は各リポジトリの `README.md` / `SETUP.md` を参照してください。
