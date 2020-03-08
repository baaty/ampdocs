---
layout: page
---

### 説明

ユーザーに通知を表示

### 使い方

    <amp-user-notification 属性>
    </amp-user-notification>

### 必要なスクリプト

    <script async custom-element="amp-user-notification" src="https://cdn.ampproject.org/v0/amp-user-notification-0.1.js"></script>

### 属性

| 属性名                 | 説明                                                   |
|------------------------|--------------------------------------------------------|
| data-show-if-href      | 通知を表示するかどうか                                        |
| data-show-if-geo       | 国グループのリストのいずれかに一致した場合にのみ                          |
| data-show-if-not-geo   | 国グループが指定されたリストと一致しない場合にのみ                       |
| data-dismiss-href      | 指定したURLへのCORS POSTリクエストを送信                         |
| data-persist-dismissal | 通知の却下を記憶しない                                      |
| enctype                | エンコードタイプ                                               |
| fallback               | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                | メディア式に基づいた要素の縦サイズ                                 |
| layout                 | レイアウト                                                  |
| media                  | メディア属性                                               |
| noloading              | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                     | イベントの実行用                                            |
| placeholder            | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                  | メディア式に基づいた要素の横サイズ                                 |
| width                  | 横幅                                                   |
| height                 | 高さ                                                    |

### アクション

| アクション名 | 説明          |
|---------|-------------|
| dismiss | ユーザー通知を閉じる |

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### 例

#### 基本的な使い方

    <amp-user-notification
      layout=nodisplay
      id="amp-user-notification1"
      data-show-if-href="https://example.com/api/show?timestamp=TIMESTAMP"
      data-dismiss-href="https://example.com/api/echo/post">
      This site uses cookies to personalize content.
      <a href="#learn-more">Learn more.</a>
     <button on="tap:amp-user-notification1.dismiss">I accept</button>
    </amp-user-notification>

#### 通知を表示するかどうか(data-show-if-href)

    <amp-user-notification
      layout=nodisplay
      id="amp-user-notification2"
      data-dismiss-href="https://example.com/api/echo/post">
      This site uses cookies to personalize content.
      <a href="#learn-more">Learn more.</a>
     <button on="tap:amp-user-notification1.dismiss">I accept</button>
    </amp-user-notification>

#### 指定したURLへのCORS POSTリクエストを送信(data-dismiss-href)

    <amp-user-notification
      layout=nodisplay
      id="amp-user-notification3"
      data-show-if-href="https://example.com/api/show?timestamp=TIMESTAMP">
      This site uses cookies to personalize content.
      <a href="#learn-more">Learn more.</a>
     <button on="tap:amp-user-notification1.dismiss">I accept</button>
    </amp-user-notification>
