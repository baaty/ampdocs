---
layout: page
---

### 説明

ストーリーに広告を動的に表示

### 使い方

    <amp-story>
      <amp-story-auto-ads>
        <script type="application/json">
          {
            設定
          }
        </script>
      </amp-story-auto-ads>
    </amp-story>

### 必要なスクリプト

    <script async custom-element="amp-story-auto-ads" src="https://cdn.ampproject.org/v0/amp-story-auto-ads-0.1.js"></script>

### トリガー

| トリガー名           | 説明                   |
|------------------|----------------------|
| story-ad-request | 広告がリクエスト             |
| story-ad-load    | 広告がロード               |
| story-ad-insert  | 広告が挿入              |
| story-ad-view    | 広告が表示              |
| story-ad-click   | 広告のCTAボタンがクリッ        |
| story-ad-exit    | ユーザーが広告を見ることをやめる    |
| story-ad-discard | 設定が無効なため、広告は破棄 |

### 変数

| 変数名      | 説明                                    |
|-------------|-----------------------------------------|
| adIndex     | トリガーを生成する広告のインデックス                  |
| adUniqueId  | ID                                      |
| requestTime | 広告がリクエストされたときのタイムスタンプ                 |
| loadTime    | 広告がINI_LOAD信号を発信するときのタイムスタンプ      |
| insertTime  | 広告がストーリーに挿入されたときのタイムスタンプ            |
| viewTime    | 広告ページがアクティブページになったときのタイムスタンプ          |
| clickTime   | 広告がクリックされたときのタイムスタンプ                  |
| exitTime    | 広告ページがアクティブ・非アクティブから移動したときのタイムスタンプ |
| discardTime | 不正なメタデータなどにより広告が破棄されたときのタイムスタンプ   |
| position    | 親ストーリー内の位置                          |
| ctaType     | 挿入された広告のCTAタイプを指定               |

### 例

#### 基本的な使い方

    <amp-story-auto-ads>
      <script type="application/json">
        {
            "ad-attributes": {
              "type": "custom",
              "data-url": "./amp-story-auto-ads-payload.json"
            }
        }
      </script>
      <template type="amp-mustache" id="template-1">
        <amp-img class="fill-img" layout="fill" src="{{imgSrc}}"></amp-img>
      </template>
    </amp-story-auto-ads>
