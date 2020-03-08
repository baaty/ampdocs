---
layout: page
---

### 説明

オートコンプリート

### 使い方

    <amp-autocomplete 属性>
      <input />
      <script type="application/json">
        {"items": 配列}
      </script>
    </amp-autocomplete>

### 必要なスクリプト

    <script async custom-element="amp-autocomplete" src="https://cdn.ampproject.org/v0/amp-autocomplete-0.1.js"></script>

### 属性

| 属性名               | 説明                                                   |
|----------------------|--------------------------------------------------------|
| filter(必須)         | フィルタリングの種類。詳しくはfilterの種類を参照                     |
| src                  | 表示されるJSONのエントリーポイント                                  |
| query                | クエリパラメータ                                               |
| filter-expr          | filter==customの場合                                    |
| filter-value         | クライアント側のフィルタ                                          |
| min-characters       | ユーザ入力の最小文字数                                     |
| max-entries          | 表示される最大アイテム数                                      |
| suggest-first        | 最初のアイテムをアクティブ                                        |
| submit-on-enter      | Enterキーで送信                                           |
| highlight-user-entry | 一致する文字をハイライト                                       |
| items                | レスポンスJSON内の配列へのキー                                   |
| inline               | インライン                                                  |
| fallback             | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights              | メディア式に基づいた要素の縦サイズ                                 |
| layout               | レイアウト                                                  |
| media                | メディア属性                                               |
| noloading            | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                   | イベントの実行用                                            |
| placeholder          | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                | メディア式に基づいた要素の横サイズ                                 |
| width                | 横幅                                                   |
| height               | 高さ                                                    |

### filter の種類

| 種類         | 説明                  |
|--------------|-----------------------|
| substring    | サブストリング               |
| prefix       | プレフィックス               |
| token-prefix | マルチワードのプレフィックス        |
| fuzzy        | タイプミスなども含む           |
| none         | なし                    |
| custom       | amp-bind ifで条件を指定 |

### イベント

| イベント名 | 説明               |
|--------|------------------|
| select | オプションが選択されたら実行 |

### レイアウト

| レイアウト名   | 説明                      |
|-----------|-------------------------|
| container | 子要素に応じて自動的にサイズ調整 |

### 例

#### 基本的な使い方

    <amp-autocomplete filter="substring" id="myAutocomplete">
      <input />
      <script type="application/json">
        {"items": ["a", "b", "c"]}
      </script>
    </amp-autocomplete>

#### 静的データ

    <amp-autocomplete filter="prefix">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### リモートデータ

    <amp-autocomplete
      filter="prefix"
      src="https://data.com/articles.json?ref=CANONICAL_URL">
      <input />
    </amp-autocomplete>

#### テキストエリア

    <amp-autocomplete
      filter="prefix"
      src="https://data.com/articles.json?ref=CANONICAL_URL">
      <textarea></textarea>
    </amp-autocomplete>

#### テキストエリアで属性あり

    <amp-autocomplete
      filter="prefix"
      src="https://data.com/articles.json?ref=CANONICAL_URL">
      <textarea autoexpand placeholder="Reply"></textarea>
    </amp-autocomplete>

#### クエリあり

    <amp-autocomplete
      filter="prefix"
      src="https://data.com/articles.json?ref=CANONICAL_URL"
      query="q">
      <input />
    </amp-autocomplete>

#### リクエスト先を動的に変更

    <amp-autocomplete filter="prefix" [src]="foo.bar">
      <input />
    </amp-autocomplete>

#### searchタイプ

    <amp-autocomplete filter="prefix">
      <input type="search" />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### filter=token-prefix

    <amp-autocomplete filter="token-prefix">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### filter=substring

    <amp-autocomplete filter="substring">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### filter=fuzzy

    <amp-autocomplete filter="fuzzy">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### filter=none

    <amp-autocomplete filter="none">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### filter=custom

    <amp-autocomplete filter="custom" filter-expr="true">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### inline=@

    <amp-autocomplete inline="@" filter="prefix">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### items=property

    <amp-autocomplete filter="prefix" items="property">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### ユーザ入力の最小文字数(min-characters)

    <amp-autocomplete filter="prefix" min-characters="3">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### 表示される最大アイテム数(max-entries)

    <amp-autocomplete filter="prefix" max-entries="10">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### 最初のアイテムをアクティブ(suggest-first)

    <amp-autocomplete suggest-first filter="prefix">
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### 一致する文字をハイライト(highlight-user-entry)

    <amp-autocomplete filter="prefix" highlight-user-entry>
      <input type="text" />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### Enterキーで送信(submit-on-enter)

    <amp-autocomplete filter="prefix" submit-on-enter>
      <input />
      <script type="application/json">
        {}
      </script>
    </amp-autocomplete>

#### テンプレートをカスタマイズ

    <amp-autocomplete filter="prefix">
      <input />
      <script type="application/json">
        {}
      </script>
      <template type="amp-mustache" id="amp-template-default">
        <div class="city-item" data-value="{{value}}">
          <div>{{value}}</div>
          <div class="custom-population">Population: {{population}}</div>
        </div>
      </template>
    </amp-autocomplete>

#### template="amp-mustache"

    <amp-autocomplete filter="prefix">
      <input />
      <script type="application/json">
        {}
      </script>
      <script type="text/plain" template="amp-mustache">
        <div class="city-item" data-value="{{value}}">
          <div>{{value}}</div>
          <div class="custom-population">Population: {{population}}</div>
        </div>
      </script>
    </amp-autocomplete>
