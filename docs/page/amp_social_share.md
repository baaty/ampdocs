---
layout: page
---

### 説明

ソーシャルシェアボタンを表示

### 使い方

    <amp-social-share 属性>
    </amp-social-share>

### 必要なスクリプト

    <script async custom-element="amp-social-share" src="https://cdn.ampproject.org/v0/amp-social-share-0.1.js"></script>

### 属性

| 属性名              | 説明                                                   |
|---------------------|--------------------------------------------------------|
| type(必須)          | プロバイダのタイプ                                              |
| data-target         | ターゲットをどこに開くのか(\_blank or \_top)                        |
| data-share-endpoint | 共有エンドポイントのURL                                        |
| data-param-\*       | 各サービスに渡すパラメータ                                        |
| fallback            | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights             | メディア式に基づいた要素の縦サイズ                                 |
| layout              | レイアウト                                                  |
| media               | メディア属性                                               |
| noloading           | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                  | イベントの実行用                                            |
| placeholder         | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes               | メディア式に基づいた要素の横サイズ                                 |
| width               | 横幅                                                   |
| height              | 高さ                                                    |

### タイプ

| タイプ名     | 説明          |
|-----------|---------------|
| system    | Web Share API |
| email     | メール           |
| facebook  | Facebook      |
| linkedin  | LinkedIn      |
| pinterest | Pinterest     |
| gplus     | Google+       |
| tumblr    | Tumblr        |
| twitter   | Twitter       |
| whatsapp  | WhatsApp      |
| line      | LINE          |
| sms       | SMS           |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| container    | 子要素に応じて自動的にサイズ調整          |
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-social-share type="twitter"></amp-social-share>

#### Email

    <amp-social-share
      type="email"
      data-param-subject="Hello World"
      data-param-body="What's up?"
      data-param-recipient="sample@xyz.com"
      aria-label="Share by email">
    </amp-social-share>

#### Twitter

    <amp-social-share
      type="twitter"
      aria-label="Share to Twitter">
    </amp-social-share>

#### Facebook

    <amp-social-share
      type="facebook"
      data-param-text="Hello world"
      data-param-href="https://example.com/?ref=URL"
      data-param-app_id="145634995501895"
      aria-label="Share to Facebook">
    </amp-social-share>

#### Line

    <amp-social-share
      type="line"
      aria-label="Share to line">
    </amp-social-share>

#### whatsapp

    <amp-social-share
      type="whatsapp"
      aria-label="Share to Whatsapp">
    </amp-social-share>

#### Pinterest

    <amp-social-share
      type="pinterest"
      data-param-media="https://lh3.googleusercontent.com/qNn8GDz8Jfd-s9lt3Nc4lJeLjVyEaqGJTk1vuCUWazCmAeOBVjSWDD0SMTU7x0zhVe5UzOTKR0n-kN4SXx7yElvpKYvCMaRyS_g-jydhJ_cEVYmYPiZ_j1Y9de43mlKxU6s06uK1NAlpbSkL_046amEKOdgIACICkuWfOBwlw2hUDfjPOWskeyMrcTu8XOEerCLuVqXugG31QC345hz3lUyOlkdT9fMYVUynSERGNzHba7bXMOxKRe3izS5DIWUgJs3oeKYqA-V8iqgCvneD1jj0Ff68V_ajm4BDchQubBJU0ytXVkoWh27ngeEHubpnApOS6fcGsjPxeuMjnzAUtoTsiXz2FZi1mMrxrblJ-kZoAq1DJ95cnoqoa2CYq3BTgq2E8BRe2paNxLJ5GXBCTpNdXMpVJc6eD7ceijQyn-2qanilX-iK3ChbOq0uBHMvsdoC_LsFOu5KzbbNH71vM3DPkvDGmHJmF67Vj8sQ6uBrLnzpYlCyN4-Y9frR8zugDcqX5Q=w400-h300-no"
      aria-label="Share to Pinterest">
    </amp-social-share>

#### Baidu

    <amp-social-share
      type="baidu"
      layout="responsive"
      width="40"
      height="40"
      data-share-endpoint="http://cang.baidu.com/do/add"
      data-param-iu="CANONICAL_URL"
      data-param-it="TITLE"
      aria-label="Share to Baidu">
      B
    </amp-social-share>

### SMS

    <amp-social-share
      type="sms"
      layout="responsive"
      width="40"
      height="40"
      aria-label="Share via SMS">
    </amp-social-share>

#### パラメータを渡す

    <amp-social-share
      type="linkedin"
      width="60"
      height="44"
      data-param-text="Hello world"
      data-param-url="https://example.com/">
    </amp-social-share>

#### data-share-endpoint

    <amp-social-share
      type="vote-this-up"
      layout="container"
      data-share-endpoint="https://example.com/vote-this-up"
      data-param-text="Check this out: TITLE - CANONICAL_URL">
      Share on Whatsapp
    </amp-social-share>

#### サイドバー

    <amp-sidebar layout="nodisplay">
      <amp-social-share
        type="vote-this-up"
        layout="container"
        data-share-endpoint="https://example.com/vote-this-up"
        data-param-text="Check this out: TITLE - CANONICAL_URL">
        Share on Whatsapp
      </amp-social-share>
    </amp-sidebar>
