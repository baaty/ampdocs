---
layout: page
---

### 説明

[Narrativ](https://narrativ.com/)の機能を表示

### 使い方

    <amp-smartlinks 属性>
    </amp-smartlinks>

### 必要なスクリプト

    <script async custom-element="amp-smartlinks" src="https://cdn.ampproject.org/v0/amp-smartlinks-0.1.js"></script>

### 属性

| 属性名                  | 説明                                                   |
|-------------------------|--------------------------------------------------------|
| nrtv-account-name(必須) | Narrativアカウント名                                        |
| linkmate                | Linkmateサービスを実行するためのフラグ                              |
| exclusive-links         | 排他的リンク                                              |
| link-attribute          | URLを異なる要素属性に保存する場合                            |
| link-selector           | 収益化するすべてのリンクを取得                                   |
| fallback                | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                 | メディア式に基づいた要素の縦サイズ                                 |
| layout                  | レイアウト                                                  |
| media                   | メディア属性                                               |
| noloading               | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                      | イベントの実行用                                            |
| placeholder             | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                   | メディア式に基づいた要素の横サイズ                                 |
| width                   | 横幅                                                   |
| height                  | 高さ                                                    |

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-smartlinks
      layout="nodisplay"
      nrtv-account-name="supercoolpublisher"
      linkmate>
    </amp-smartlinks>

#### 属性あり

    <amp-smartlinks
      layout="nodisplay"
      nrtv-account-name="examplepublisher"
      linkmate
      exclusive-links
      link-attribute="href"
      link-selector="a">
    </amp-smartlinks>
