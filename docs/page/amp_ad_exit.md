---
layout: page
---

### 説明

広告内の他の要素に終了を指定

### 使い方

    <amp-ad-exit id="アクション名">
      <script type="application/json">
        {
          フィルターの設定
        }
      </amp-ad-exit>
    </amp-ad-exit>

### 必要なスクリプト

    <script async custom-element="amp-ad-exit" src="https://cdn.ampproject.org/v0/amp-ad-exit-0.1.js"></script>

### フィルター

| フィルター名    | 説明                               |
| --------------- | ---------------------------------- |
| clickLocation   | 縁からの最小距離                   |
| clickDelay      | クリックに応答する前に待機する時間 |
| inactiveElement | 終了が発生しない                   |

#### clickLocationのフィルター

| フィルター名 | 説明               |
| ------------ | ------------------ |
| top          | 上端からの距離(px) |
| right        | 右端からの距離(px) |
| bottom       | 下端からの距離(px) |
| left         | 左端からの距離(px) |
| relativeTo   | 境界に使用する要素 |

#### clickDelayのフィルター

| フィルター名     | 説明                                                 |
| ---------------- | ---------------------------------------------------- |
| delay            | ビューポートに入ってからクリックを拒否するまでの時間 |
| startTimingEvent | 遅延開始間隔として使用するイベントの名前             |

#### inactiveElementのフィルター

| フィルター名 | 説明           |
| ------------ | -------------- |
| selector     | CSSセレクター |

### アクション

| アクション名    | 説明                                                          |
| --------------- | ------------------------------------------------------------- |
| target          | ターゲット                                                    |
| \[a-zA-Z0-9-\]+ | URLパラメータをこの名前と値に置き換えて、最終URLと追跡URL |

### レイアウト

| レイアウト名 | 説明                             |
| ------------ | -------------------------------- |
| container    | 子要素に応じて自動的にサイズ調整 |
| nodisplay    | 要素が非表示                     |

### 例

#### 基本的な使い方

    <amp-ad-exit id="exit-api">
      <script type="application/json">
        {
          "targets": {
            "landingPage": {
              "finalUrl": "https://example.com/artisan-baking/?from=_clickArea",
              "vars": {
                "_clickArea": {
                  "defaultValue": "headline"
                }
              }
            },
            "flour": {
              "finalUrl": "https://adclickserver.example.com/click?id=af319adec901&x=CLICK_X&y=CLICK_Y&adurl=https://example.com/artisan-baking/flour",
              "filters": ["3sClick", "borderProtection"],
              "behaviors": {
                "clickTarget": "_top"
              }
            },
            "bannetons": {
              "finalUrl": "https://example.com/artisan-baking/bannetons",
              "trackingUrls": [
                "https://adclickserver.example.com/click?id=af319adec901&x=CLICK_X&y=CLICK_Y",
                "https://tracker.adnetwork.example.com/?url=example.com"
              ],
              "filters": ["3sClick", "borderProtection"]
            }
          },
          "filters": {
            "3sClick": {
              "type": "clickDelay",
              "delay": 3000
            },
            "borderProtection": {
              "type": "clickLocation",
              "top": 10,
              "right": 10,
              "bottom": 10,
              "left": 10
            }
          }
        }
      </script>
    </amp-ad-exit>
    <h1 on="tap:exit-api.exit(target='landingPage')">Artisan Baking Supplies</h1>
    <div id="product0" on="tap:exit-api.exit(target='flour')">
      <p>Rye flour</p>
      <amp-img src="..." width="..." height="..."></amp-img>
    </div>
    <div id="product1" on="tap:exit-api.exit(target='bannetons')">
      <p>Bannetons</p>
      <amp-img src="..." width="..." height="..."></amp-img>
    </div>
    <div id="footer" on="tap:exit-api.exit(target='landingPage', _clickArea='footer')">
      example.com/artisan-baking
    </div>

### フィルタ

    <amp-ad-exit id="exit-api">
    <script type="application/json">
      {
        "targets": {
          "ad": {
          "finalUrl": "...",
          "filters": ["2second", "huge-border"]
          }
        },
        "filters": {
          "2second": {
            "type": "clickDelay",
            "delay": 2000
          },
          "small-border": {
            "type": "clickLocation",
            "top": 5,
            "right": 5,
            "bottom": 5,
            "left": 5
          },
          "huge-border": {
            "type": "clickLocation",
            "top": 100,
            "right": 100,
            "bottom": 100,
            "left": 100
          },
          "border-with-relative-to-element": {
            "type": "clickLocation",
            "top": 10,
            "right": 10,
            "bottom": 10,
            "left": 10,
            "relativeTo": "#headline"
          }
        }
      }
    </script>
    </amp-ad-exit>
