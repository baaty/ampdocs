---
layout: page
---

### 説明

データを動的に読み込み、指定したテンプレートを使って動的に表示

### 使い方

    <amp-live-list 属性>
    </amp-live-list>

### 必要なスクリプト

    <script async custom-element="amp-live-list" src="https://cdn.ampproject.org/v0/amp-live-list-0.1.js"></script>

### 属性

| 属性名                  | 説明                                                   |
|-------------------------|--------------------------------------------------------|
| id(必須)                | ID                                                     |
| data-poll-interval      | 新しいコンテンツのチェック間隔(ミリ秒)                               |
| data-max-items-per-page | 1ページあたりの最大データ数                                      |
| disabled                | 無効化                                                 |
| fallback                | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                 | メディア式に基づいた要素の縦サイズ                                 |
| layout                  | レイアウト                                                  |
| media                   | メディア属性                                               |
| noloading               | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                      | イベントの実行用                                            |
| placeholder             | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                   | メディア式に基づいた要素の横サイズ                                 |
| width                   | 横幅                                                   |
| height                  | 高さ                                                    |

### items の属性

| 属性名               | 説明        |
|----------------------|-------------|
| id(必須)             | 子のID       |
| data-sort-time(必須) | 並べ替え時間  |
| data-update-time     | 更新時間    |
| data-tombstone       | 削除されたアイテム |
| sort                 | ソート         |

### アクション

| アクション名 | 説明           |
|---------|--------------|
| update  | 更新された時に実行 |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| container    | 子要素に応じて自動的にサイズ調整          |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |

### 例

#### 基本的な使い方

    <amp-live-list
      id="my-live-list"
      data-max-items-per-page="20">
      <button update on="tap:my-live-list.update">You have updates!</button>
      <div items></div>
      <div pagination></div>
    </amp-live-list>

#### data-poll-intervalとdata-max-items-per-page

    <amp-live-list
      data-poll-interval="15000"
      data-max-items-per-page="20"
      id="my-live-list-1">
      <button update>You have updates!</button>
      <ul items>
        <li id="1" data-sort-time="42" data-update-time="42">1</li>
        <li id="2" data-sort-time="43" data-update-time="44">2</li>
      </ul>
      <div pagination></div>
    </amp-live-list>

#### ボタンで更新

    <amp-live-list
      id="my-live-list-3"
      data-poll-interval="15000"
      data-max-items-per-page="20">
      <button update on="tap:my-live-list.update">You have updates!</button>
      <button update on="tap:my-live-list.update">You have updates!</button>
      <div items></div>
      <div pagination></div>
      <div pagination></div>
    </amp-live-list>
