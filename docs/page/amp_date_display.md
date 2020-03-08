---
layout: page
---

### 説明

時間を表示

### 使い方

    <amp-date-display 属性>
    </amp-date-display>

### 必要なスクリプト

    <script async custom-element="amp-date-display" src="https://cdn.ampproject.org/v0/amp-date-display-0.1.js"></script>

### 属性

| 属性名            | 説明                                                   |
|-------------------|--------------------------------------------------------|
| datetime          | 日付時刻                                               |
| timestamp-ms      | タイムスタンプ(ミリ秒)                                          |
| timestamp-seconds | タイムスタンプ(秒)                                            |
| locale            | ロケール                                                   |
| display-in        | UTCに変換                                               |
| offset-seconds    | オフセット                                                  |
| fallback          | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights           | メディア式に基づいた要素の縦サイズ                                 |
| layout            | レイアウト                                                  |
| media             | メディア属性                                               |
| noloading         | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                | イベントの実行用                                            |
| placeholder       | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes             | メディア式に基づいた要素の横サイズ                                 |
| width             | 横幅                                                   |
| height            | 高さ                                                    |

### 時間の形式

| フォーマット         | 説明                                     |
|----------------|------------------------------------------|
| day            | 1, 2, ...12, 13, etc.                    |
| dayName        | 文字列                                   |
| dayNameShort   | 文字列                                   |
| dayPeriod      | string,                                  |
| dayTwoDigit    | 01, 02, 03, ..., 12, 13, etc.            |
| hour           | 0, 1, 2, 3, ..., 12, 13, ..., 22, 23     |
| hour12         | 1, 2, 3, ..., 12, 1, 2, ..., 11, 12      |
| hour12TwoDigit | 01, 02, ..., 12, 01, 02, ..., 11, 12     |
| hourTwoDigit   | 00, 01, 02, ..., 12, 13, ..., 22, 23     |
| iso            | ISO8601                                  |
| minute         | 0, 1, 2, ..., 58, 59                     |
| minuteTwoDigit | 00, 01, 02, ..., 58, 59                  |
| month          | 1, 2, 3, ..., 12                         |
| monthName      | 国際化された月名文字列                      |
| monthNameShort | 国際化された短縮月名文字列                  |
| monthTwoDigit  | 01, 02, ..., 11, 12                      |
| second         | 0, 1, 2, ..., 58, 59                     |
| secondTwoDigit | 00, 01, 02, ..., 58, 59                  |
| year           | 0, 1, 2, ..., 1999, 2000, 2001, etc.     |
| yearTwoDigit   | 00, 01, 02, ..., 17, 18, 19, ..., 98, 99 |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-date-display
      datetime="2017-08-02T15:05:05.000Z"
      layout="fixed"
      width="360"
      height="20">
      <template type="amp-mustache">{{iso}}</template>
    </amp-date-display>

#### タイムスタンプ(timestamp-seconds)

    <amp-date-display
      timestamp-seconds="1501686305"
      layout="fixed"
      width="360"
      height="20">
      <template type="amp-mustache">{{iso}}</template>
    </amp-date-display>

#### タイムスタンプ(timestamp-ms)

    <amp-date-display
      timestamp-ms="1501686305000"
      layout="fixed"
      width="360"
      height="20">
      <template type="amp-mustache">{{iso}}</template>
    </amp-date-display>

#### UTC に変換(display-in)

    <amp-date-display
      display-in="utc"
      datetime="now"
      layout="fixed"
      width="360"
      height="20">
      <template type="amp-mustache">{{iso}}</template>
    </amp-date-display>

#### テンプレート(template)

    <amp-date-display
      template="myTemplate"
      datetime="now"
      display-in="utc"
      layout="fixed"
      width="360"
      height="20">
    </amp-date-display>
    <template type="amp-mustache" id="myTemplate">{{iso}}</template>
