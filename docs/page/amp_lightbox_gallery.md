---
layout: page
---

### 説明

閉じるまで表示されるライトボックスを表示

### 使い方

#### amp-img

    <amp-img lightbox amp-imgの属性></amp-img>

#### amp-carousel

    <amp-carousel lightbox amp-carouselの属性></amp-carousel>

### 必要なスクリプト

    <script async custom-element="amp-lightbox-gallery" src="https://cdn.ampproject.org/v0/amp-lightbox-gallery-0.1.js"></script>

### 例

#### 基本的な使い方

    <amp-img
      src="/awesome.png"
      width="300"
      height="300"
      lightbox>
    </amp-img>

#### amp-video

    <amp-video
      lightbox
      src="../av/ForBiggerJoyrides-short.mp4"
      width="720"
      height="405"
      layout="responsive"
      controls>
    </amp-video>

#### amp-youtube

    <amp-youtube
      lightbox
      data-videoid="lBTCB7yLs8Y"
      width="358"
      height="204"
      layout="responsive">
    </amp-youtube>

#### amp-carousel

    <amp-carousel
      width=400
      height=300
      layout="responsive"
      type=slides
      lightbox>
    </amp-carousel>
