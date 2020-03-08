---
layout: page
---

### 説明

様々なAMPタグやHTMLタグで使える共通の属性について

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
| fallback    | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights     | メディア式に基づいた要素の縦サイズ                                 |
| layout      | レイアウト                                                  |
| media       | メディア属性                                               |
| noloading   | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on          | イベントの実行用                                            |
| placeholder | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes       | メディア式に基づいた要素の横サイズ                                 |
| width       | 横幅                                                   |
| height      | 高さ                                                    |

### 例

#### fallback

    <amp-anim src="animated.gif" width="466" height="355" layout="responsive" >
      <div fallback>この端末ではアニメーション画像は再生できません。</div>
    </amp-anim>

#### heights

    <amp-img
      heights="(min-width:500px) 200px, 80%"
      src="amp.png"
      width="320"
      height="256">
    </amp-img>

#### layout

    <amp-img
      layout="responsive"
      src="/img/amp.jpg"
      width="1080"
      height="610"
      alt="画像">
    </amp-img>

#### media

    <amp-img
      media="(min-width: 650px)"
      src="wide.jpg"
      width="466"
      height="355"
      layout="responsive">
    </amp-img>

#### noloading

    <amp-img
      src="card.jpg"
      noloading
      height="190"
      width="297"
      layout="responsive">
    </amp-img>

#### on

    <button
      on="tap:my-lightbox">
      ライトボックスを開く
    </button>

#### placeholder

    <amp-anim src="animated.gif" width="466" height="355" layout="responsive">
      <amp-img placeholder src="preview.png" layout="fill"></amp-img>
    </amp-anim>

#### sizes

    <amp-img
      sizes="(min-width: 320px) 320px, 100vw"
      src="amp.png"
      width="400"
      height="300"
      layout="responsive">
    </amp-img>

#### widthとheight

    <amp-anim
      width="245"
      height="300"
      src="/img/cat.gif"
      alt="猫のアニメーション">
    </amp-anim>
