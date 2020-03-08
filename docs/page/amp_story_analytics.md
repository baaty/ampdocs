---
layout: page
---

### 説明

ストーリー分析

### 使い方

    <amp-story-analytics 属性>
    </amp-story-analytics>

### 必要なスクリプト

    <script async custom-element="amp-story" src="https://cdn.ampproject.org/v0/amp-story-0.1.js"></script>

### トリガー

#### 構造

    "triggers": {
      "ストーリー名": {
        "on": "イベント名",
        "request": "リクエスト"
      }
    }

### ストーリー

| 名前                          | 説明                                                                     |
| ----------------------------- | ------------------------------------------------------------------------ |
| storyPageId                   | ストーリーページID                                                      |
| storyPageIndex                | ストーリーページのゼロベースのインデックス値                             |
| storyPageCount                | ページの総数                                                             |
| storyProgress                 | ストーリーのユーザーの進行状況                                           |
| storyIsMuted                  | ストーリーがミュートされたかどうか                                       |
| storyBookendComponentPosition | ユーザーがクリックしたブックエンドコンポーネントのインデックスを表す数値 |
| storyBookendComponentType     | クリックされたブックエンドのコンポーネントのタイプ                       |
| storyBookendTargetHref        | クリックされたブックエンドコンポーネントのURL                           |

#### イベント

| イベント名                  | 説明                                         |
| --------------------------- | -------------------------------------------- |
| story-page-visible          | ページが表示されたときにイベントが実行       |
| story-last-page-visible     | 最後のページがユーザーに表示されたときに実行 |
| story-bookend-enter         | ブックエンドの入力後に実行                   |
| story-bookend-exit          | ブックエンドの離脱後に実行                   |
| story-bookend-click         | ブックエンド内でクリックしたら実行           |
| story-audio-muted           | ミュートしたら実行                           |
| story-audio-unmuted         | ミュートを解除したら実行                     |
| story-page-attachment-enter | 添付ファイルを開いたら実行                   |
| story-page-attachment-exit  | 添付ファイルをキャンセルしたら実行           |

### 例

#### 基本的な使い方

    <amp-analytics>
      <script type="application/json">
        {
          "requests": {
            "pageview": "https://foo.com/pixel?RANDOM"
          },
          "triggers": {
            "trackPageview": {
              "on": "visible",
              "request": "pageview"
            }
          }
        }
      </script>
    </amp-analytics>
