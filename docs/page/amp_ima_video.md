---
layout: page
---

### 説明

IMA SDKに統合されているインストリーム動画広告用の動画プレーヤーを表示

### 使い方

    <amp-ima-video 属性>
    </amp-ima-video>

### 必要なスクリプト

    <script async custom-element="amp-ima-video" src="https://cdn.ampproject.org/v0/amp-ima-video-0.1.js"></script>

### 属性

| 属性名                | 説明                                                   |
|-----------------------|--------------------------------------------------------|
| data-tag(必須)        | VAST広告ドキュメントのURL                                     |
| data-src              | ビデオコンテンツの RL                                           |
| data-crossorigin      | クロスホストを許可するか                                         |
| data-poster           | ビデオの再生が開始される前に表示されるフレームの画像                    |
| data-delay-ad-request | 広告リクエストを遅延                                         |
| data-ad-label         | 広告の再生時に広告を表示するために使用                         |
| dock                  | 最小化するか                                              |
| fallback              | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights               | メディア式に基づいた要素の縦サイズ                                 |
| layout                | レイアウト                                                  |
| media                 | メディア属性                                               |
| noloading             | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                    | イベントの実行用                                            |
| placeholder           | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                 | メディア式に基づいた要素の横サイズ                                 |
| width                 | 横幅                                                   |
| height                | 高さ                                                    |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-ima-video
      width=640
      height=360
      layout="responsive"
      autoplay
      data-src="https://s0.2mdn.net/4253510/google_ddm_animation_480P.mp4"
      data-tag="https://pubads.g.doubleclick.net/gampad/ads?sz=640x480&iu=/124319096/external/ad_rule_samples&ciu_szs=300x250&ad_rule=1&impl=s&gdfp_req=1&env=vp&output=vmap&unviewed_position_start=1&cust_params=deployment%3Ddevsite%26sample_ar%3Dpremidpost&cmsid=496&vid=short_onecue&correlator="
      data-poster="path/to/poster.png">
    </amp-ima-video>
