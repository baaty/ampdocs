---
layout: page
---

### 説明

日付を Twitter などで使われる「3 時間前」などのフォーマットに変換

### 使い方

    <amp-timeago 属性>
    </amp-timeago>

### 必要なスクリプト

    <script async custom-element="amp-timeago" src="https://cdn.ampproject.org/v0/amp-timeago-0.1.js"></script>

### 属性

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
| datetime    | 日付と時刻(ISO datetime)                                |
| locale      | ロケール                                                   |
| cutoff      | 指定された日付を秒単位で渡して表示                            |
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

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-timeago
      layout="fixed"
      width="160"
      height="20"
      datetime="2017-04-11T00:37:33.809Z"
      locale="en"
      cutoff="8640000">
      Saturday 11 April 2017 00.37
    </amp-timeago>

#### ロケール(locale)

    <amp-timeago
      layout="fixed"
      width="160"
      height="20"
      datetime="2017-08-11T18:58:58.000Z"
      locale="fr" cutoff="8640000">
      Lundi 14 août 2017
    </amp-timeago>

#### 指定された日付を秒単位で渡して表示(cutoff)

    <amp-timeago
      layout="fixed"
      width="160"
      height="20"
      datetime="2017-04-11T00:37:33.809Z">
      Saturday 11 April 2017 00.37
    </amp-timeago>
