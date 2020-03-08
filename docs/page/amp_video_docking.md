---
layout: page
---

### 説明

動画を最小化する機能を追加

### 使い方

    <amp-video-docking 属性>
    </amp-video-docking>

### 必要なスクリプト

    <script async custom-element="amp-video-docking" src="https://cdn.ampproject.org/v0/amp-video-docking-0.1.js"></script>

### サポート

- amp-brightcove
- amp-dailymotion
- amp-delight-player
- amp-ima-video
- amp-video
- amp-video-iframe
- amp-youtube

### 例

#### amp-youtube

    <amp-youtube
      dock
      layout=fill
      width=300
      height=500
      data-videoid="dQw4w9WgXcQ">
    </amp-youtube>

#### amp-brightcove

    <amp-brightcove
      dock
      data-account="1290862519001"
      data-video-id="ref:amp-docs-sample"
      data-player-id="SyIOV8yWM"
      layout="responsive" width="480" height="270">
    </amp-brightcove>

#### amp-dailymotion

    <amp-dailymotion
      dock
      data-videoid="x2m8jpp" width="500" height="281">
    </amp-dailymotion>

#### amp-delight-player

    <amp-delight-player
      data-content-id="-LLoCCZqWi18O73b6M0w"
      layout="fixed"
      width="960"
      height="540"
      dock>
    </amp-delight-player>

#### amp-ima-video

    <amp-ima-video
      dock
      width=640 height=360 layout="responsive"
      data-src="https://s0.2mdn.net/4253510/google_ddm_animation_480P.mp4"
      data-tag="https://pubads.g.doubleclick.net/gampad/ads?sz=640x480&iu=/124319096/external/ad_rule_samples&ciu_szs=300x250&ad_rule=1&impl=s&gdfp_req=1&env=vp&output=vmap&unviewed_position_start=1&cust_params=deployment%3Ddevsite%26sample_ar%3Dpremidpost&cmsid=496&vid=short_onecue&correlator="
      data-poster="path/to/poster.png">
    </amp-ima-video>

#### amp-video-iframe

    <amp-video-iframe
      dock
      layout=fill
      width=300
      height=500
      poster="https://foo.com/image.png"
      src="https://foo.com/video">
    </amp-video-iframe>

#### amp-video

    <amp-video
      dock
      layout=fill
      width=300
      height=500
      controls>
    </amp-video>
