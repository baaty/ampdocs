---
layout: page
---

### 説明

カレンダーウィジェットを表示

### 使い方

    <amp-date-picker 属性>
    </amp-date-picker>

### 必要なスクリプト

    <script async custom-element="amp-date-picker" src="https://cdn.ampproject.org/v0/amp-date-picker-0.1.js"></script>

### 属性

| 属性名                        | 説明                                                   | デフォルト値              |
|-------------------------------|--------------------------------------------------------|----------------------|
| mode                          | カレンダーのモード                                              | static               |
| type                          | カレンダーのタイプ                                              | single               |
| input-selector                | 入力フィールド                                              | 非表示フィールドを自動生成 |
| start-input-selector          | 開始日入力フィールド                                        | 非表示フィールドを自動生成 |
| end-input-selector            | 終了日入力フィールド                                        | 非表示フィールドを自動生成 |
| min                           | 選択できる最も早い日付                                      | 現在の日付            |
| max                           | 選択できる最も遅い日付                                      | なし                   |
| month-format                  | 月の形式                                                | MMMM YYYY            |
| format                        | 入力フィールドのフォーマット                                       | YYYY-MM-DD           |
| week-day-format               | 平日のフォーマット                                            |                      |
| locale                        | ロケール                                                   | en                   |
| maximum-nights                | 日付範囲内でユーザーが選択できる夜の数                           | 0                    |
| minimum-nights                | 日付範囲で選択する必要がある夜の数                            | 1                    |
| number-of-months              | 一度に表示する月数                                        | 1                    |
| first-day-of-week             | 週の最初の日                                             | 0(日曜日)            |
| blocked                       | ユーザーがカレンダーで選択できない                                    |                      |
| highlighted                   | ハイライト                                                  |                      |
| day-size                      | 日付セルのサイズ(px)                                         | 39                   |
| allow-blocked-end-date        | 開始日の選択後に終了日を選択                              |                      |
| allow-blocked-ranges          | 範囲指定                                               |                      |
| src                           | JSONを取得するURL                                         |                      |
| fullscreen                    | 全画面表示                                             |                      |
| open-after-select             | 日付を選択後もカレンダーを開き続ける                              |                      |
| open-after-clear              | 日付をクリア後もカレンダーを開き続ける                               |                      |
| hide-keyboard-shortcuts-panel | ピッカーの下部にあるキーボードショートカットパネルを非表示                     |                      |
| fallback                      | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |                      |
| heights                       | メディア式に基づいた要素の縦サイズ                                 |                      |
| layout                        | レイアウト                                                  |                      |
| media                         | メディア属性                                               |                      |
| noloading                     | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |                      |
| on                            | イベントの実行用                                            |                      |
| placeholder                   | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |                      |
| sizes                         | メディア式に基づいた要素の横サイズ                                 |                      |
| width                         | 横幅                                                   |                      |
| height                        | 高さ                                                    |                      |

### イベント

| イベント名     | 説明                      |
|------------|-------------------------|
| activate   | カレンダーがアクティブになった時に実行    |
| deactivate | カレンダーがアクティブではなくなった時に実行 |
| select     | 日付が選択された時に実行       |

### アクション

| アクション名    | 説明           |
|------------|----------------|
| clear      | クリア            |
| setDate    | 日付が選択      |
| setDates   | 日付を範囲指定  |
| today      | 現在の日付が選択 |
| startToday | 開始日が選択    |
| endToday   | 終了日が選択    |

### 表示モード

| モード名         | 説明                            |
|---------------|-------------------------------|
| static(デフォルト) | 静的なカレンダー                      |
| overlay       | 必須の入力フィールドを操作後にカレンダー表示 |

### タイプ

| タイプ名  | 説明          |
|--------|-------------|
| single | 一日指定      |
| range  | 範囲で日付指定 |

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

#### 基本的な使い方

    <amp-date-picker
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### 必須の入力フィールドを操作後にカレンダー表示(overlay)

    <amp-date-picker
      mode="overlay"
      input-selector="[name=date1]">
      <input type="text" name="date1">
    </amp-date-picker>

#### 静的なカレンダー(static)

    <amp-date-picker
      mode="static"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### 一日指定(single)

    <amp-date-picker
      type="single"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### 範囲で日付指定(range)

    <amp-date-picker
      type="range"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### 複数要素

    <amp-date-picker
      type="range"
      mode="overlay"
      start-input-selector="[name=date2]"
      end-input-selector="[name=date3]">
      <input type="text" name="date2">
      <input type="text" name="date3">
    </amp-date-picker>

#### 入力フィールド(input-selector)

    <amp-date-picker
      input-selector="#a1"
      type="single"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### 全画面表示(fullscreen)

    <amp-date-picker
      fullscreen
      mode="static"
      layout="fill">
    </amp-date-picker>

#### 日付セルのサイズ(day-size)

    <amp-date-picker
      day-size="50"
      type="range"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### 一度に表示する月数(number-of-months)

    <amp-date-picker
      number-of-months="12"
      type="range"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### 週の最初の日(first-day-of-week)

    <amp-date-picker
      first-day-of-week="1"
      type="range"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### JSONを取得するURL(src)

    <amp-date-picker
      src="https://data.com/dates.json?ref=CANONICAL_URL"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### テンプレート(template)

    <amp-date-picker
      layout="fixed-height"
      height="360">
      <template type="amp-mustache" date-template default>{{D}}</template>
    </amp-date-picker>

#### 日付範囲内でユーザーが選択できる夜の数(maximum-nights)

    <amp-date-picker
      maximum-nights="3"
      type="range"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### 日付範囲で選択する必要がある夜の数(minimum-nights)

    <amp-date-picker
      minimum-nights="0"
      type="range"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### start-dateとend-date

    <amp-date-picker
      start-date="2018-01-01"
      end-date="2018-01-01"
      type="range"
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### touch-keyboard-editable

    <amp-date-picker
      touch-keyboard-editable
      mode="overlay"
      input-selector="#a4">
      <input id="a4">
    </amp-date-picker>

#### maxとmin

     <amp-date-picker
       [min]="min"
       [max]="max"
       layout="fixed-height"
       height="360">
    </amp-date-picker>

#### 開始日の選択後に終了日を選択(allow-blocked-end-date)

    <amp-date-picker
      allow-blocked-end-date
      layout="fixed-height"
      height="360">
    </amp-date-picker>

#### ピッカーの下部にあるキーボードショートカットパネルを非表示(hide-keyboard-shortcuts-panel)

    <amp-date-picker
      hide-keyboard-shortcuts-panel
      layout="fixed-height"
      height="360">
    </amp-date-picker>
