---
layout: page
---

### 説明

[Soundcloud](https://soundcloud.com/)の音声プレーヤーを表示

### 使い方

    <amp-soundcloud 属性>
    </amp-soundcloud>

### 必要なスクリプト

    <script async custom-element="amp-soundcloud" src="https://cdn.ampproject.org/v0/amp-soundcloud-0.1.js"></script>

### 属性

| 属性名             | 説明                                                   |
|--------------------|--------------------------------------------------------|
| data-trackid(必須) | トラックID                                                 |
| data-playlistid    | プレイリストID                                               |
| data-secret-token  | シークレットトークン                                             |
| data-visual        | データビジュアルモード                                            |
| data-color         | ウィジェットの色                                              |
| width              | 横幅                                                   |
| height             | 高さ                                                    |
| layout             | レイアウト                                                  |
| fallback           | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights            | メディア式に基づいた要素の縦サイズ                                 |
| layout             | レイアウト                                                  |
| media              | メディア属性                                               |
| noloading          | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                 | イベントの実行用                                            |
| placeholder        | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes              | メディア式に基づいた要素の横サイズ                                 |
| width              | 横幅                                                   |
| height             | 高さ                                                    |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| intrinsic    | 指定したアスペクト比に自動的にサイズ調整       |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### Visual Mode

    <amp-soundcloud
      width="480"
      height="480"
      layout="responsive"
      data-trackid="243169232"
      data-visual="true">
    </amp-soundcloud>

#### Classic Mode

    <amp-soundcloud
      width="480"
      height="480"
      layout="responsive"
      data-trackid="243169232"
      data-color="ff5500">
    </amp-soundcloud>
