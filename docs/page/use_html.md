---
layout: page
---

### HTMLタグ

| タグ名       | 説明                            |
|------------|---------------------------------|
| html       | ルート要素                         |
| head       | メタデータの記述                      |
| title      | ページのタイトル                        |
| link       | 関連したURLに関しての情報。一部に制限あり |
| meta       | 一部に制限あり                     |
| style      | 内部スタイルシート。一部に制限あり         |
| body       | コンテンツの記述                      |
| article    | 完結したコンテンツ                     |
| section    | 汎用的なセクション                    |
| nav        | ナビゲーション                         |
| aside      | 補足や関連情報                   |
| h1         | 見出し                           |
| h2         | 見出し                           |
| h3         | 見出し                           |
| h4         | 見出し                           |
| h5         | 見出し                           |
| h6         | 見出し                           |
| header     | ヘッダー                            |
| footer     | フッター                            |
| address    | コンテンツに関するお問い合わせ先            |
| p          | パラグラフ                           |
| hr         | 区切り文字                       |
| pre        | 整形済みテキスト                     |
| blockquote | 引用                            |
| ol         | 順番付きリスト                      |
| ul         | 順不同なリスト                      |
| li         | リストの各項目                      |
| dl         | 説明リスト                         |
| dt         | 語句                            |
| dd         | 語句の説明                       |
| figure     | フィギュア                           |
| figcaption | フィギュアのキャプション                    |
| div        | 汎用タグ                          |
| main       | メインコンテンツ                        |
| em         | 強調                            |
| strong     | 重要                            |
| small      | 但し書き                          |
| s          | 変更                            |
| cite       | 作品のタイトルなど                     |
| q          | 引用                            |
| dfn        | 定義する語句                      |
| abbr       | 略語                            |
| data       | マシンリーダブルな情報                   |
| time       | 日時                            |
| code       | コンピュータコード                       |
| var        | 変数                            |
| samp       | コンピュータからの出力内容               |
| kbd        | コンピュータへの入力内容                |
| sub        | 上付き                           |
| sup        | 下付き                           |
| i          | 学名や慣用句など                   |
| b          | ちゅうもくしてほし語句                   |
| u          | 不明瞭な語句                     |
| mark       | ハイライト                           |
| ruby       | ルビ                              |
| rb         | ルビのベース                          |
| rt         | ルビ                              |
| rtc        | ルビのコンテナ                         |
| rp         | ルビに未対応なブラウザ用                |
| bdi        | 双方向アルゴリズムの隔離               |
| bdo        | 双方向アルゴリズムのオーバーライド            |
| span       | 汎用タグ                          |
| br         | 改行                            |
| wbr        | 改行を認める箇所                   |
| ins        | 追加したコンテンツ                     |
| del        | 削除したコンテンツ                     |
| source     | メディアリソース                        |
| table      | テーブル                            |
| caption    | フローコンテンツ                        |
| colgroup   | 列のグループ                         |
| col        | 列に属性やスタイルを指定               |
| tbody      | 行のグループ                         |
| thead      | 行のグループ                         |
| tfoot      | 行のグループ                         |
| tr         | テーブルの行                         |
| td         | テーブルのデータ                        |
| th         | テーブルの見出し                      |
| form       | フォーム。一部に制限あり                |
| input      | 各種入力フォーム。一部に制限あり        |
| button     | ボタン                             |
| script     | スクリプト。一部に制限あり               |
| noscript   | スクリプトが動作しないブラウザ用の情報        |
| a          | リンク。一部に制限あり                 |

### 制限があるHTMLタグ

| タグ名   | 補足                                                                                                                            |
|--------|---------------------------------------------------------------------------------------------------------------------------------|
| script | タイプが「application/ld+json」または「text/plain」 のみ                                                                                     |
| form   | amp-formと組み合わせることが必要                                                                                                        |
| input  | タイプが「password」または「file」以外は使用可能                                                                                            |
| style  | amp-boilerplate以外でHEADタグ内で1つのみが使用可能。style amp-customのように指定                                                             |
| link   | [microformats.org](http://microformats.org/wiki/existing-rel-values)に登録されているものだけ使用可能。<link rel=”＜許可された文字列＞”>のように指定 |
| meta   | 「http-equiv」属性以外は使用可能。「http-equiv」は特定の値でのみ                                                                           |
| a      | 原則として利用可能。「href」属性で「javascript:」で始まることはNG、「target」属性は「\_blank」のみ                                                     |
| svg    | 一部のSVG要素が禁止                                                                                                               |

## 使えない HTML タグ

| タグ名     | 補足                |
|----------|---------------------|
| base     |                     |
| img      | 代わりにamp-imgを使用   |
| picture  |                     |
| video    | 代わりにamp-videoを使用 |
| audio    | 代わりにamp-audioを使用 |
| iframe   | 代わりにamp-ifameを使用 |
| frame    |                     |
| frameset |                     |
| object   |                     |
| param    |                     |
| applet   |                     |
| embed    |                     |
