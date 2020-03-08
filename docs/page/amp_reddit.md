---
layout: page
---

### 説明

Reddit の投稿やコメントを表示

### 使い方

    <amp-reddit 属性>
    </amp-reddit>

### 必要なスクリプト

    <script async custom-element="amp-reddit" src="https://cdn.ampproject.org/v0/amp-reddit-0.1.js"></script>

### 属性

| 属性名               | 説明                                                   |
|----------------------|--------------------------------------------------------|
| data-embedtype(必須) | タイプ                                                    |
| data-src(必須)       | 投稿またはコメントのパーマリンク                                     |
| height(必須)         | 高さ                                                    |
| width(必須)          | 横幅                                                   |
| data-uuid            | コメント埋め込み用に提供されたUUID                               |
| data-embedcreated    | コメントの埋め込みの日時文字列                                 |
| data-embedlive       | コメントの埋め込みの日時文字列                                 |
| data-embedparent     | 埋め込みコメントを更新するかどうか                                  |
| fallback             | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights              | メディア式に基づいた要素の縦サイズ                                 |
| layout               | レイアウト                                                  |
| media                | メディア属性                                               |
| noloading            | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                   | イベントの実行用                                            |
| placeholder          | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                | メディア式に基づいた要素の横サイズ                                 |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 投稿

    <amp-reddit
      layout="responsive"
      width="300"
      height="400"
      data-embedtype="post"
      data-src="https://www.reddit.com/r/me_irl/comments/52rmir/me_irl/?ref=share&amp;ref_source=embed">
    </amp-reddit>

#### コメント

    <amp-reddit
      layout="responsive"
      width="400"
      height="400"
      data-embedtype="comment"
      data-src="https://www.reddit.com/r/sports/comments/54loj1/50_cents_awful_1st_pitch_given_a_historical/d8306kw"
      data-uuid="b1246282-bd7b-4778-8c5b-5b08ac0e175e"
      data-embedcreated="2016-09-26T21:26:17.823Z"
      data-embedparent="true"
      data-embedlive="true">
    </amp-reddit>
