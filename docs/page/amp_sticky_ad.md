---
layout: page
---

### 説明

画面下部に常時表示される広告を表示

### 使い方

    <amp-sticky-ad 属性>
    </amp-sticky-ad>

### 必要なスクリプト

    <script async custom-element="amp-sticky-ad" src="https://cdn.ampproject.org/v0/amp-sticky-ad-1.0.js"></script>

### 属性

| 属性名       | 説明                                                   |
|--------------|--------------------------------------------------------|
| layout(必須) | レイアウト                                                  |
| fallback     | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights      | メディア式に基づいた要素の縦サイズ                                 |
| layout       | レイアウト                                                  |
| media        | メディア属性                                               |
| noloading    | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on           | イベントの実行用                                            |
| placeholder  | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes        | メディア式に基づいた要素の横サイズ                                 |
| width        | 横幅                                                   |
| height       | 高さ                                                    |

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### ルール

- amp-sticky-adは最大で1つ
- amp-sticky-adは、直接の子要素に1つのamp-adが必須
- 広告はページの下部に表示
- 広告の高さは100px以下
- amp-sticky-adの横幅は100%
- amp-sticky-adの不透明度は1
- amp-sticky-adの背景色は不透明
- 広告はビューポート1つ分をスクロールした後に表示
- 広告は一番下までスクロールしたら非表示
- 横長モードの場合に広告は中央揃え
- 広告がない場合は表示されない

### 例

#### 基本的な使い方

    <amp-sticky-ad layout=nodisplay>
      <amp-ad
        width=300
        height=250
        type="a9"
        data-aax_size="300x250"
        data-aax_pubname="test123"
        data-aax_src="302">
      </amp-ad>
    </amp-sticky-ad>
