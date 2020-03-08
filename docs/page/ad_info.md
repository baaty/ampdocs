---
layout: page
--- 

### 広告について

今までのWebページ(非AMPページ)では、JavaScriptのコードをページに追加して広告の表示を行っていた。  
AMPページではパフォーマンスとセキュリティ上の理由から専用のタグを使って広告を表示する。

### 簡単な手順

ここでは例として、a9ネットワークの広告を追加する時の手順

#### amp-adスクリプトを追加

    <script async custom-element="amp-ad" src="https://cdn.ampproject.org/v0/amp-ad-0.1.js"></script>

#### amp-adタグを追加

    <amp-ad type="a9">
    </amp-ad>

#### サイズを追加

    <amp-ad
      width="300"
      height="250"
      type="a9">
    </amp-ad>

#### 広告ごとに必要なパラメータを追加

    <amp-ad
      data-aax_size="300x250"
      data-aax_pubname="test123"
      data-aax_src="302"
      type="a9"
      width="300"
      height="250">
    </amp-ad>

#### プレースホルダを指定(省略可)

    <amp-ad type="a9" width="300" height="250" data-aax_size="300x250" data-aax_pubname="test123" data-aax_src="302">
      <amp-img
        placeholder
        src="placeholder-image.jpg">
      </amp-img>
    </amp-ad>

#### フォールバックを指定(省略可)

    <amp-ad type="a9" width="300" height="250" data-aax_size="300x250" data-aax_pubname="test123" data-aax_src="302">
      <amp-img fallback src="fallback-image.jpg"></amp-img>
    </amp-ad>
