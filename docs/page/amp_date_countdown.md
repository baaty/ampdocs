---
layout: page
---

### 説明

指定した時間までの残り時間を表示

### 使い方

    <amp-date-countdown 属性>
    </amp-date-countdown>

### 必要なスクリプト

    <script async custom-element="amp-date-countdown" src="https://cdn.ampproject.org/v0/amp-date-countdown-0.1.js"></script>

### 属性

| 属性名            | 説明                                                   |
|-------------------|--------------------------------------------------------|
| end-date(必須)    | 終了日                                                 |
| timestamp-ms      | タイムスタンプ(ミリ秒)                                          |
| timestamp-seconds | タイムスタンプ(秒)                                            |
| timeleft-ms       | 残された秒数(ミリ秒)                                        |
| offset-seconds    | オフセット                                                  |
| when-ended        | 終了時にタイマーを停止するか                                    |
| locale            | ロケール                                                   |
| biggest-unit      | 最大単位                                               |
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

### イベント

| イベント名  | 説明            |
|---------|---------------|
| timeout | タイムアウトした時に実行 |

### 時間の形式

| フォーマット  | 説明               |
|---------|-------------------|
| d       | 日: 0、1、2、...      |
| dd      | 日: 00、01、02、03 .. |
| h       | 時間: 0、1、2、...    |
| hh      | 時間: 01、02、03 ..  |
| m       | 分: 0、1、2、...      |
| mm      | 分: 01、01、02、03 .. |
| ss      | 秒: 00、01、02、03 .. |
| days    | 日の国際化文字列    |
| hours   | 時間の国際化文字列  |
| minutes | 分の国際化文字列    |
| seconds | 秒の国際化文字列    |

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

    <amp-date-countdown
      timestamp-seconds="2147483648"
      layout="fixed-height"
      height="50">
      <template type="amp-mustache">
        <p class="p1">
          {{d}} days, {{h}} hours, {{m}} minutes and {{s}} seconds until
          <a href="https://en.wikipedia.org/wiki/Year_2038_problem">Y2K38</a>.
        </p>
      </template>
    </amp-date-countdown>

#### テンプレート

    <template type="amp-mustache" id="myTemplate">
      <div class="date-count-down">
        \{\{#d\}\} \{\{d\}\} <span>\{\{days\}\}</span> \{\{/d\}\}
        \{\{h\}\} <span>\{\{hours\}\}</span>
        \{\{m\}\} <span>\{\{minutes\}\}</span>
        \{\{s\}\} <span>\{\{seconds\}\}</span>
      </div>
    </template>
    <amp-date-countdown timestamp-ms="1521880470000" offset-seconds="1521880470" when-ended="stop" locale='zh-tw' height="50" width="360" template="myTemplate">
    </amp-date-countdown>
