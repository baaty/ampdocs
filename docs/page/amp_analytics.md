---
layout: page
---

### 説明

アクセス解析の設定や送信

### 使い方

    <amp-analytics [属性]>
      <script type="application/json">
        {
          設定
        }
      </script>
    </amp-analytics>

### 必要なスクリプト

    <script async custom-element="amp-analytics" src="https://cdn.ampproject.org/v0/amp-analytics-0.1.js"></script>

### 属性

| 属性名 | 説明             |
| ------ | ---------------- |
| type   | タイプ名         |
| config | 設定データの URL |

### 設定

| 名前      | 説明                 |
| --------- | -------------------- |
| requests  | 送信するデータの種類 |
| triggers  | 送信するタイミング   |
| transport | 送信方法             |

### transportの要素

| 属性名  | 説明                                               |
| ------- | -------------------------------------------------- |
| beacon  | リクエストの送信にnavigator.sendBeaconが使用可能 |
| xhrpost | リクエストの送信にXMLHttpRequestが使用可能       |
| image   | Imageタグを生成することでリクエストを送信可能     |

### データ

| 属性名         | 説明                                   |
| -------------- | -------------------------------------- |
| baseUrl        | リクエストURL                         |
| reportWindow   | リクエストのレポートを停止する期間(秒) |
| batchInterval  | 実行する間隔(秒)                       |
| extraUrlParams | リクエストパラメータ                   |

### トリガー

| 名前                            | 説明                                                                                                                           |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| on(必須)                        | 実行するイベント。有効な値は、render-start、ini-load、click、scroll、timer、visible、hidden、user-error、access-_\*、video-_\* |
| request(必須)                   | 送信するリクエストの名前                                                                                                       |
| vars                            | Key-Value オブジェクト                                                                                                         |
| important                       | バッチ処理の動作やレポート期間                                                                                                 |
| selector、selectionMethod       | 一部のトリガーに対して指定可能                                                                                                 |
| scrollSpec(scroll の場合は必須) | scroll トリガーと組み合わせて使用                                                                                              |
| timerSpec(timer の場合は必須)   | timer トリガーと組み合わせて使用                                                                                               |
| sampleSpec                      | リクエストを送信する前にサンプリングする方法を定義                                                                             |
| videoSpec                       | video-\*トリガーと組み合わせて使用                                                                                             |

### 変数

| 変数名                       | 説明                               |
| ---------------------------- | ---------------------------------- |
| \${ampdocHost}               | AMPドキュメントホスト             |
| \${ampdocHostname}           | AMPドキュメントのホスト名         |
| \${ampdocUrl}                | AMPドキュメントのURL             |
| \${canonicalHost}            | 正規ホスト                         |
| \${canonicalHostname}        | 正規のホスト名                     |
| \${canonicalPath}            | 正規パス                           |
| \${canonicalUrl}             | 正規URL                           |
| \${counter}                  | カウンター                         |
| \${documentCharset}          | ドキュメントの文字セット           |
| \${documentReferrer}         | ドキュメントリファラー             |
| \${externalReferrer}         | 外部リファラー                     |
| \${htmlAttr}                 | HTML属性                          |
| \${sourceUrl}                | ソースURL                         |
| \${sourceHost}               | 送信元ホスト                       |
| \${sourceHostname}           | 送信元ホスト名                     |
| \${sourcePath}               | ソースパス                         |
| \${title}                    | タイトル                           |
| \${viewer}                   | 視聴者                             |
| \${contentLoadTime}          | コンテンツの読み込み時間           |
| \${domainLookupTime}         | ドメイン検索時間                   |
| \${domInteractiveTime}       | DOMインタラクティブタイム         |
| \${navRedirectCount}         | ナビゲーションリダイレクトカウント |
| \${navTiming}                | ナビゲーションのタイミング         |
| \${navType}                  | ナビゲーションタイプ               |
| \${pageDownloadTime}         | ページのダウンロード時間           |
| \${pageLoadTime}             | ページ読み込み時間                 |
| \${redirectTime}             | リダイレクト時間                   |
| \${serverResponseTime}       | サーバー応答時間                   |
| \${tcpConnectTime}           | TCP接続時間                       |
| \${availableScreenHeight}    | 利用可能なスクリーンの高さ         |
| \${availableScreenWidth}     | 利用可能な画面幅                   |
| \${browserLanguage}          | ブラウザ言語                       |
| \${screenColorDepth}         | 画面の色深度                       |
| \${screenHeight}             | スクリーンの高さ                   |
| \${screenWidth}              | スクリーン幅                       |
| \${scrollHeight}             | スクロール高さ                     |
| \${scrollWidth}              | スクロール幅                       |
| \${scrollLeft}               | 左にスクロール                     |
| \${scrollTop}                | スクロールトップ                   |
| \${timezone}                 | タイムゾーン                       |
| \${timezoneCode}             | タイムゾーンコード                 |
| \${userAgent}                | ユーザーエージェント               |
| \${viewportHeight}           | ビューポートの高さ                 |
| \${viewportWidth}            | ビューポート幅                     |
| \${horizontalScrollBoundary} | 水平スクロール境界                 |
| \${totalEngagedTime}         | 合計エンゲージメント時間           |
| \${incrementalEngagedTime}   | 増分関与時間                       |
| \${verticalScrollBoundary}   | 垂直スクロール境界                 |
| \${backgrounded}             | バックグラウンド                   |
| \${backgroundedAtStart}      | 開始時の背景                       |
| \${fromSlide}                | スライドからのカルーセル           |
| \${toSlide}                  | カルーセルをスライドさせる         |
| \${elementId}                | 要素ID                            |
| \${elementHeight}            | エレメントの高さ                   |
| \${elementWidth}             | エレメント幅                       |
| \${elementX}                 | 要素X                             |
| \${elementY}                 | 要素Y                             |
| \${firstSeenTime}            | 初めて見た時間                     |
| \${firstVisibleTime}         | 最初の表示時間                     |
| \${initialScrollDepth}       | 初期スクロール深度                 |
| \${intersectionRatio}        | 交差比率                           |
| \${intersectionRect}         | 交差点の長方形                     |
| \${lastSeenTime}             | 最後に見た時間                     |
| \${lastVisibleTime}          | 最終表示時刻                       |
| \${loadTimeVisibility}       | ロード時間の可視性                 |
| \${maxContinuousVisibleTime} | 最大連続可視時間                   |
| \${maxScrollDepth}           | 最大スクロール深度                 |
| \${maxVisiblePercentage}     | 最大可視パーセンテージ             |
| \${minVisiblePercentage}     | 最小可視パーセンテージ             |
| \${totalTime}                | 合計時間                           |
| \${totalVisibleTime}         | 合計可視時間                       |
| \${timerDuration}            | タイマー持続時間                   |
| \${timerStart}               | タイマー開始時間                   |
| \${ampVersion}               | AMPバージョン                     |
| \${ampState}                 | AMPの状態                         |
| \${backgroundState}          | バックグラウンド状態               |
| \${clientId}                 | クライアントID                    |
| \${extraUrlParams}           | 追加のURLパラメーター            |
| \${pageViewId}               | ページビューID                    |
| \${pageViewId64}             | ページビューID 64                 |
| \${queryParam}               | クエリパラメータ                   |
| \${random}                   | ランダム                           |
| \${requestCount}             | リクエスト数                       |
| \${timestamp}                | タイムスタンプ                     |
| \${errorName}                | エラー名                           |
| \${errorMessage}             | エラーメッセージ                   |

### タイプ

| タイプ名                | 説明                                                                  |
| ----------------------- | --------------------------------------------------------------------- |
| googleanalytics         | Googleアナリティクス                                                 |
| acquialift              | Acquia Lift                                                           |
| adobeanalytics          | Adobe Analytics                                                       |
| afsanalytics            | AFS Analytics                                                         |
| alexametrics            | AT Internet                                                           |
| baiduanalytics          | Baidu Analytics                                                       |
| burt                    | Burt                                                                  |
| chartbeat               | Chartbeat                                                             |
| clicky                  | Clicky Web Analytics                                                  |
| comscore                | comScore Unified Digital Measurement                                  |
| cxense                  | Cxense Insight                                                        |
| dynatrace               | Dynatraceのリアルユーザーモニタリング                                |
| euleriananalytics       | オイラーテクノロジーアナリティクス                                    |
| facebookpixel           | Facebookピクセル                                                     |
| gemius                  | Gemius Audience/Gemius Prismの分析                                   |
| googleadwords           | Google AdWordsのコンバージョントラッキングやリマーケティング         |
| infonline               | INFOnlineやIVW                                                      |
| krux                    | Krux                                                                  |
| linkpulse               | Linkpulse                                                             |
| lotame                  | Lotame                                                                |
| mediametrie             | Médiamétrieのトラッキングページ                                      |
| mediarithmics           | mediarithmics                                                         |
| mparticle               | mParticle                                                             |
| newrelic                | New Relic Browserを利用してAMPのスループットとパフォーマンスを測定 |
| nielsen                 | Nielsen DCR                                                           |
| nielsen-marketing-cloud | Nielsen Marketing Cloud                                               |
| oewa                    | OEWA                                                                  |
| parsely                 | Parsely                                                               |
| piano                   | Piano                                                                 |
| quantcast               | Quantcast Measurement                                                 |
| segment                 | Segment                                                               |
| mpulse                  | SOASTA mPulse                                                         |
| simplereach             | Snowplow Analytics                                                    |
| top100                  | Rambler/TOP-100                                                       |
| topmailru               | Top.Mail.Ru                                                           |
| umenganalytics          | Umeng+ Analytics                                                      |
| treasuredata            | Treasure Data                                                         |
| webtrekk_2              | Webtrekk                                                              |
| metrika                 | Yandex Metrica                                                        |

### 例

#### googleanalytics

    <amp-analytics type="googleanalytics" id="analytics1">
      <script type="application/json">
        {
          "vars": {
            "account": "UA-XXXXX-Y"  // Replace with your property ID.
          },
          "triggers": {
            "trackPageview": {  // Trigger names can be any string. trackPageview is not a required name.
              "on": "visible",
              "request": "pageview"
            }
          }
        }
      </script>
    </amp-analytics>

#### 第三者へ送信

    <amp-analytics type="nielsen">
      <script type="application/json">
      {
        "vars": {
          "apid": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
          "apv": "1.0",
          "apn": "My AMP Website",
          "section": "Entertainment",
          "segA": "Music",
          "segB": "News",
          "segC": "Google AMP"
        }
      }
      </script>
    </amp-analytics>

#### URLで送信

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

#### 2秒ごとに送信

    <amp-analytics>
    <script type="application/json">
    {
      "requests": {
        "timer": {
          "baseUrl": "https://example.com/analytics?",
          "batchInterval": 2,
        }
      }
      "triggers": {
        "timer": {
          "on": "timer",
          "request" : "timer",
          "timerSpec": {
            "interval": 1
          },
          "extraUrlParams": {
            "rc": "${requestCount}"
          }
        }
      }
    }
    </script>
    </amp-analytics>

#### 50%のリクエストでサンプリング

    <amp-analytics>
    <script type="application/json">
    {
      "requests": {
        "pageview": "https://foo.com/pixel?RANDOM"
      },
      'triggers': {
        'sampledOnRandom': {
          'on': 'visible',
          'request': 'request',
          'sampleSpec': {
            'sampleOn': '${random}',
            'threshold': 50
          }
        }
      }
    }
    </script>
    </amp-analytics>
