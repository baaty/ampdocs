---
layout: page
---

### 説明

広告を表示  
amp-adの別名  
amp-adを推奨

### 使い方

    <amp-embed 属性>
    </amp-embed>

### 必要なスクリプト

    <script async custom-element="amp-ad" src="https://cdn.ampproject.org/v0/amp-ad-0.1.js"></script>

### 属性

| 属性名                       | 説明                                                   |
|------------------------------|--------------------------------------------------------|
| type(必須)                   | 広告の種類                                              |
| src                          | 広告のスクリプトタグ                                           |
| data-\*                      | 広告ごとの詳細設定                                        |
| json                         | JSON形式のオプションが必要な場合                               |
| data-consent-notification-id | 通知関連                                               |
| data-loading-strategy        | 別の要素の広告に対して読み込みを開始するよう指示                   |
| fallback                     | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                      | メディア式に基づいた要素の縦サイズ                                 |
| layout                       | レイアウト                                                  |
| media                        | メディア属性                                               |
| noloading                    | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                           | イベントの実行用                                            |
| placeholder                  | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                        | メディア式に基づいた要素の横サイズ                                 |
| width                        | 横幅                                                   |
| height                       | 高さ                                                    |

### 広告の種類

- 1wo
- 24smi
- a8
- a9
- accesstrade
- adagio
- adblade
- adbutler
- adform
- adfox
- adgeneration
- adglare
- adhese
- adincube
- adition
- adman
- admanmedia
- admixer
- adocean
- adop
- adpicker
- adplugg
- adpon
- adreactor
- adsensor
- adservsolutions
- adsloom
- adsnative
- adspeed
- adspirit
- adstir
- adstyle
- adtech
- adthrive
- adunity
- aduptech
- adventive
- adverline
- adverticum
- advertserve
- adyoulike
- affiliateb
- aja
- amoad
- aniview
- appnexus
- appvador
- atomx
- baidu
- beaverads
- bidtellect
- blade
- brainy
- bringhub
- broadstreetads
- byplay
- caajainfeed
- capirs
- caprofitx
- cedato
- colombia
- conative
- connatix
- contentad
- criteo
- dable
- dianomi
- directadvert
- distroscale
- dotandads
- dynad
- eadv
- eas
- empower
- engageya
- epeex
- eplanning
- ezoic
- f1e
- f1h
- felmat
- flite
- fluct
- forkmedia
- freewheel
- fusion
- genieessp
- giraff
- gmossp
- gumgum
- holder
- ibillboard
- idealmedia
- imedia
- imobile
- imonomy
- improvedigital
- industrybrains
- inmobi
- innity
- insticator
- invibes
- ix
- jubna
- kargo
- kiosked
- kixer
- kuadio
- lentainform
- ligatus
- lockerdome
- logly
- loka
- mads
- mantis
- medianet
- mediavine
- medyanet
- meg
- mgid
- microad
- miximedia
- mixpo
- monetizer101
- mox
- mytarget
- mywidget
- nativeroll
- nativery
- nativo
- navegg
- nend
- netletix
- noddus
- nokta
- nws
- onead
- onnetwork
- openadstream
- openx
- opinary
- outbrain
- pixels
- plista
- polymorphicads
- popin
- postquare
- pressboard
- promoteiq
- pubexchange
- pubguru
- pubmatic
- pubmine
- puffnetwork
- pulsepoint
- purch
- quoraad
- rbinfox
- readmo
- realclick
- recomad
- relap
- revcontent
- revjet
- rfp
- rnetplus
- rubicon
- runative
- sas
- seedingalliance
- sekindo
- sharethrough
- shemedia
- sklik
- slimcutmedia
- smartadserver
- smartclip
- smi2
- smilewanted
- sogouad
- sortable
- sovrn
- speakol
- spotx
- springAds
- ssp
- strossle
- sulvo
- sunmedia
- svknative
- swoop
- taboola
- tcsemotion
- teads
- temedya
- torimochi
- tracdelight
- triplelift
- trugaze
- uas
- ucfunnel
- unruly
- uzou
- valuecommerce
- vdoai
- videointelligence
- videonow
- viralize
- vmfive
- webediads
- weborama
- whopainfeed
- widespace
- wisteria
- wpmedia
- xlift
- yahoo
- yahoojp
- yahoonativeads
- yandex
- yengo
- yieldbot
- yieldmo
- yieldone
- yieldpro
- zedo
- zen
- zergnet
- zucks

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

#### AdSense

    <amp-embed
      width="100vw"
      height="320"
      type="adsense"
      data-ad-client="ca-pub-2005682797531342"
      data-ad-slot="7046626912"
      data-auto-format="rspv"
      data-full-width>
      <div overflow></div>
    </amp-embed>

#### Yahoo JP

    <amp-embed
      width="320"
      height="50"
      type="yahoojp"
      data-yadsid="79712_113431">
    </amp-embed>

#### カスタム

    <amp-embed
      width=300
      height=250
      type="custom"
      data-url="https://foobar.com"
      template="template-1">
    </amp-embed>
