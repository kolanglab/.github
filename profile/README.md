# kolanglab

**言語処理系（コンパイラ・インタプリタ・GC など）を題材にした技術書・教材**を公開しています。
「作って理解する」ことを目標に、手を動かしながら読める本を揃えています。
主に、笹田が講義をするための副読本として用意しています。
言語処理系開発者として、（名前だけでも）知っておくと良さそうかなぁというものをまとめています。

すべて Claude code による自動生成テキストです。人間がレビューしている部分としていない部分がありますので、眉に唾をつけながら読んでください（AI 生成という性質上、内容の正確性は保証できませんが、気づいた誤りは可能な範囲で直します。指摘も歓迎します）。特に、引用されている論文・参考文献・実装の挙動などは、AI が実在しないものを作り出したり（ハルシネーション）、内容を誤って要約したりすることがあります。重要なところは必ず一次情報にあたってご確認ください。

本文を選択すると、GitHub による Issue 登録ボタンが出てくるので、内容に疑問や改善提案があれば、それをご利用ください。
受講者からの Issue は、AI が自動で対応します。例えば、疑問に対しては解答が、修正リクエストについては加筆修正 PR が自動で生成されます。

## 📚 本・教材

言語処理系入門がメインで、それ以外は副読本になります。
笹田が知りたい領域を主にまとめています。

| 本 | 内容 | 読む |
|--- |---   |---   |
| **言語処理系入門** | 簡単な言語を作りながら、構文解析・意味解析から VM・各種言語機能・最適化・JIT まで処理系づくりの全体像を一望する入門 | [📖 公開版](https://kolanglab.github.io/book_langimpl_intro/) ／ [repo](https://github.com/kolanglab/book_langimpl_intro) |
| **言語処理系を作りたい人のためのC言語入門** | 処理系を書くために必要な C を、目的から逆算して学ぶ | [📖 公開版](https://kolanglab.github.io/book_clang_intro/) ／ [repo](https://github.com/kolanglab/book_clang_intro) |
| **構文解析入門** | AST の作り方を、簡単な文法からパーサージェネレータ・理論・最先端まで網羅する入門 | [📖 公開版](https://kolanglab.github.io/book_parser_intro/) ／ [repo](https://github.com/kolanglab/book_parser_intro) |
| **言語処理系の意味解析入門** | AST に対する名前解決・型検査/推論・制御/データフロー解析・抽象解釈を紹介 | [📖 公開版](https://kolanglab.github.io/book_semantic_intro/) ／ [repo](https://github.com/kolanglab/book_semantic_intro) |
| **コード生成入門** | AST 取得後のコード生成を、IR・命令選択・レジスタ割り当て・最適化・JIT までコンパイラ視点で | [📖 公開版](https://kolanglab.github.io/book_code_gen/) ／ [repo](https://github.com/kolanglab/book_code_gen) |
| **最適化入門** | 言語処理系の最適化を、ピープホールから全プログラム解析まで静的言語も動的言語も区別なく一望。IR・データフロー解析の土台から SSA・ループ最適化・インライン展開・インラインキャッシュ・投機的最適化・レジスタ割り当て、equality saturation や superoptimization・機械学習による最適化まで | [📖 公開版](https://kolanglab.github.io/book_opt/) ／ [repo](https://github.com/kolanglab/book_opt) |
| **JITコンパイル入門** | なぜ JIT で速くなるのかという原理から、トレーシング・メタトレーシング・階層的 JIT・脱最適化まで、最新研究と各処理系のケーススタディも交え動くコードで | [📖 公開版](https://kolanglab.github.io/book_jit_intro/) ／ [repo](https://github.com/kolanglab/book_jit_intro) |
| **言語処理系のデータ構造入門** | シンボルテーブル・AST・値表現など処理系内部のデータ構造から、文字列・配列・ハッシュなど言語が提供するデータ型の実装まで | [📖 公開版](https://kolanglab.github.io/book_data_design/) ／ [repo](https://github.com/kolanglab/book_data_design) |
| **言語処理系における I/O 入門** | 言語処理系が必要とする I/O を、OS のシステムコール・バッファリング・ブロッキング/多重化・非同期 I/O・io_uring まで実装視点で | [📖 公開版](https://kolanglab.github.io/book_lang_io/) ／ [repo](https://github.com/kolanglab/book_lang_io) |
| **並行・並列言語処理系入門** | 言語に並列・並行機能を載せ、処理系内部（GC・共有状態・キャッシュ・GIL）を並列実行に耐えさせるまで | [📖 公開版](https://kolanglab.github.io/book_parallel_lang/) ／ [repo](https://github.com/kolanglab/book_parallel_lang) |
| **ELF/DWARF 入門** | 実行ファイル形式 ELF とデバッグ情報形式 DWARF を、ヘッダ・セクション・シンボルから行番号情報・限界まで仕様に踏み込み、自作ツールのハンズオンも交えて解説 | [📖 公開版](https://kolanglab.github.io/book_elf_dwarf/) ／ [repo](https://github.com/kolanglab/book_elf_dwarf) |
| **デバッガ開発入門** | 簡単な言語処理系を題材に、ブレークポイント・ステップ実行・状態検査などデバッガの仕組みと作り方を解説 | [📖 公開版](https://kolanglab.github.io/book_debugger_intro/) ／ [repo](https://github.com/kolanglab/book_debugger_intro) |
| **malloc 入門** | malloc/free の裏側を、API・OS インターフェースから、フリーリスト・サイズクラス・バディ/スラブの基本アルゴリズム、断片化・マルチスレッド・セキュリティ・最新研究、dlmalloc/glibc/jemalloc/TCMalloc/mimalloc など実ライブラリの設計まで、研究論文を引きながら | [📖 公開版](https://kolanglab.github.io/book_malloc/) ／ [repo](https://github.com/kolanglab/book_malloc) |
| **精密 GC をインタプリタに実装する** | インタプリタに正確な（precise）GC を実装する | [📖 公開版](https://kolanglab.github.io/book_precise_gc/) ／ [repo](https://github.com/kolanglab/book_precise_gc) |
| **保守的GC入門** | 保守的 GC を libgc で作る方法と、その裏側の理論 | [📖 公開版](https://kolanglab.github.io/book_Conservative_GC/) ／ [repo](https://github.com/kolanglab/book_Conservative_GC) |
| **GC最前線** | GC 実装方式の研究と実装、2026年時点の最前線を詳説 | [📖 公開版](https://kolanglab.github.io/book_gc_details/) ／ [repo](https://github.com/kolanglab/book_gc_details) |

## 💬 フィードバック・質問

各本の **Issue** から、誤り・わかりにくい点・疑問をどうぞ。
公開ページでは本文を選択して「Report as issue」からも送れます。

寄せられた質問や指摘は、内容に応じて回答・本文修正に反映していきます。
受講者は **質問 → 議論 → 修正の提案・反映** まで、AI 支援を受けてリポジトリ上で行えます。

## 受講者以外の方について

受講者向けのテキストですが、関係ない方も興味があればどうぞ読んでください。
AI 生成テキストなので、間違いがあるかもしれません。その点は注意して読んでください。
また、間違いを見つけたら教えていただけると幸いです。

受講者と同等の AI サポートを受けたい方は、笹田までご連絡ください（[Sponsor @ko1 on GitHub Sponsors](https://github.com/sponsors/ko1)）。

これを使った授業・講習などのご依頼も歓迎します。

## 🛠 ビルドについて

各本は [ligarb](https://github.com/ko1/ligarb) で Markdown から生成しています。
ローカルでのビルド手順は各リポジトリの `README.md` / `SETUP.md` を参照してください。