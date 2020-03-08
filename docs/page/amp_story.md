---
layout: page
---

### 説明

ストーリーページを表示

### 使い方

    <amp-story 属性>
      <amp-story-page 属性>
        <amp-story-grid-layer 属性>
        </amp-story-grid-layer>
      </amp-story-page>
    </amp-story>

### 必要なスクリプト

    <script async custom-element="amp-story" src="https://cdn.ampproject.org/v0/amp-story-1.0.js"></script>

### amp-story の属性

| 属性名                    | 説明                                                   |
|---------------------------|--------------------------------------------------------|
| standalone(必須)          | ストーリーであることの識別子                                      |
| title(必須)               | ストーリーのタイトル                                             |
| publisher(必須)           | ストーリーのパブリッシャーの名前                                     |
| publisher-logo-src(必須)  | パブリッシャーのロゴへのURL                                        |
| poster-portrait-src(必須) | サムネイル画像へのURL(3x4)                                    |
| poster-square-src         | サムネイル画像へのURL(1x1)                                    |
| poster-landscape-src      | サムネイル画像へのURL(4x3)                                    |
| supports-landscape        | 横向きのサポートを有効                                        |
| background-audio          | 音声ファイルへの RL                                          |
| live-story                | ライブストーリー機能を有効                                      |
| live-story-disabled       | ライブストーリー機能を無効                                      |
| data-poll-interval        | 新しいコンテンツのチェック間の時間間隔（ミリ秒）                        |
| fallback                  | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                   | メディア式に基づいた要素の縦サイズ                                 |
| layout                    | レイアウト                                                  |
| media                     | メディア属性                                               |
| noloading                 | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                        | イベントの実行用                                            |
| placeholder               | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                     | メディア式に基づいた要素の横サイズ                                 |
| width                     | 横幅                                                   |
| height                    | 高さ                                                    |

### アニメーション属性

| 属性                       | 説明           |
|----------------------------|----------------|
| animate-in                 | 出現           |
| animate-in-duration        | 出現期間       |
| animate-in-timing-function | アニメーションカーブ     |
| animate-in-delay           | 開始する前の遅延  |
| animate-in-after           | チェーンまたはシーケンス   |
| scale-start                | 開始           |
| scale-end                  | 終了           |
| translate-x                | 画像の水平を指定 |
| translate-y                | 画像の垂直を指定 |

### アニメーション効果

| 効果名          | 説明         |
|-----------------|--------------|
| drop-in         | ドロップイン       |
| fade-in         | フェードイン       |
| fly-in-bottom   | 下に移動      |
| fly-in-left     | 左に移動      |
| fly-in-right    | 右に移動      |
| fly-in-top      | 上に移動      |
| rotate-in-left  | 左回転       |
| rotate-in-right | 右回転       |
| twirl-in        | 回転         |
| whoosh-in-left  | 左のヒューシュ効果 |
| whoosh-in-right | 右のヒューシュ効果 |
| pan-left        | 左にスライド      |
| pan-right       | 右にスライド      |
| pan-down        | 下にスライド      |
| pan-up          | 上にスライド      |
| zoom-in         | ズームイン        |
| zoom-out        | ズームアウト       |

### 例

#### 基本的な使い方

    <amp-story standalone>
      <amp-story-page id="cover" auto-advance-after="5s">
        <amp-story-grid-layer template="vertical">
          <h1>Hello World</h1>
          <p>This is the cover page of this story.</p>
        </amp-story-grid-layer>
      </amp-story-page>
      <amp-story-page id="page-1" auto-advance-after="5s">
        <amp-story-grid-layer template="vertical">
          <h1>First Page</h1>
          <p>This is the first page of this story.</p>
        </amp-story-grid-layer>
      </amp-story-page>
      <amp-story-page id="page-2">
        <amp-story-grid-layer template="vertical">
          <h1>Second Page</h1>
          <p>This is the second page of this story.</p>
        </amp-story-grid-layer>
      </amp-story-page>
    </amp-story>

#### bookend

    <amp-story
      title="Helloworld-bookend amp-story example"
      publisher="The AMP Team"
      publisher-logo-src="https://example.com/logo/1x1.png"
      poster-portrait-src="https://example.com/my-story/poster/3x4.jpg"
      poster-square-src="https://example.com/my-story/poster/1x1.jpg"
      poster-landscape-src="https://example.com/my-story/poster/4x3.jpg"
      standalone>
      <amp-story-page id="cover">
        <amp-story-grid-layer template="vertical">
          <h1>Cover page - manual advance</h1>
          <p>3 page story with a bookend at the end</p>
        </amp-story-grid-layer>
      </amp-story-page>
      <amp-story-page id="page-1" auto-advance-after="3s">
        <amp-story-grid-layer template="vertical">
          <h1>Page 1 - auto advance after 3s</h1>
        </amp-story-grid-layer>
      </amp-story-page>
      <amp-story-page id="page-2">
        <amp-story-grid-layer template="vertical">
          <h1>Page 2 - manual advance</h1>
        </amp-story-grid-layer>
      </amp-story-page>
      <amp-story-bookend src="./bookendv1.json" layout=nodisplay>
      </amp-story-bookend>
    </amp-story>

#### zoom-in

    <amp-story standalone>
      <amp-story-grid-layer template="fill">
        <div animate-in="zoom-in" animate-in-duration="30s" scale-start="1" scale-end="3" class="img-container">
          <amp-img id="ken-burns-img1" src="https://picsum.photos/1600/1200?image=1077" animate-in="pan-left" animate-in-duration="30s"
            layout="fixed" width="1600" height="1200">
          </amp-img>
        </div>
      </amp-story-grid-layer>
    </amp-story>

#### fade-in

    <amp-story standalone>
      <div animate-in="fade-in" animate-in-after="ken-burns-img2" animate-in-duration="1s" class="img-container">
        <div animate-in="zoom-out" animate-in-duration="5s" class="img-container" animate-in-after="ken-burns-img2">
          <amp-img id="ken-burns-img3" src="https://picsum.photos/1600/1200?image=1026" layout="fixed" width="1600" height="1200" animate-in="pan-down"
            animate-in-duration="5s" animate-in-after="ken-burns-img2">
          </amp-img>
        </div>
      </div>
    </amp-story>

#### amp-story-auto-ads

    <amp-story standalone supports-landscape>
      <amp-story-auto-ads>
        <script type="application/json">
          {
            "ad-attributes": {
              "type": "doubleclick",
              "data-slot": "/30497360/a4a/amp_story_dfp_example"
            }
          }
        </script>
      </amp-story-auto-ads>
      <amp-story-page id="page-1">
        <amp-story-grid-layer class="container" template="vertical">
          <p class="num">1</p>
        </amp-story-grid-layer>
      </amp-story-page>
    </amp-story>

#### live-story

    <amp-story id="story1" live-story
      standalone
      publisher="AMP Team"
      title="Live Story"
      publisher-logo-src="https://example.com/logo/1x1.png"
      poster-portrait-src="https://example.com/my-story/poster/3x4.jpg"
      poster-square-src="https://example.com/my-story/poster/1x1.jpg"
      poster-landscape-src="https://example.com/my-story/poster/4x3.jpg">
      <amp-story-page id="cover" data-sort-time="1552330790">
        <amp-story-grid-layer template="vertical">
          <p>Append a new page!</p>
        </amp-story-grid-layer>
      </amp-story-page>
    </amp-story>

#### consent

    <amp-story standalone publisher-logo-src="https://placekitten.com/g/64/64">
      <amp-consent id='ABC' layout='nodisplay'>
        <script type="application/json">{
          "consents": {
            "DEF": {
              "checkConsentHref": "http://localhost:8000/get-consent-v1",
              "promptUI": "ui0"
            }
          }
        }</script>
        <amp-story-consent id="ui0" layout="nodisplay">
          <script type="application/json">{
            "title": "Headline.",
            "message": "This is some more information about this choice. Here's a list of items related to this choice.",
            "vendors": ["Item 1", "Item 2", "Item 3", "Item 4", "Item 5", "Item 6", "Item 7", "Item 8", "Item 9", "Item 10"],
            "externalLink": {
              "title": "Data Privacy Settings",
              "href": "https://example.com"
            }
          }</script>
        </amp-story-consent>
      </amp-consent>
      <amp-story-page id="cover" auto-advance-after="5s">
        <amp-story-grid-layer template="vertical">
          <h1>You just accepted or rejected the consent!</h1>
        </amp-story-grid-layer>
      </amp-story-page>
      <amp-story-bookend src="bookendv1.json" layout="nodisplay">
      </amp-story-bookend>
    </amp-story>
