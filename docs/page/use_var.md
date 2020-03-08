---
layout: page
---

### 使える変数

| 変数名                   | 説明                        |
|--------------------------|-----------------------------|
| AMPDOC_HOST              | AMPドキュメントホスト                |
| AMPDOC_HOSTNAME          | AMPドキュメントのホスト名             |
| AMPDOC_URL               | AMPドキュメントのURL               |
| CANONICAL_HOST           | 正規ホスト                     |
| CANONICAL_HOSTNAME       | 正規のホスト名                  |
| CANONICAL_PATH           | 正規パス                      |
| CANONICAL_URL            | 正規URL                     |
| COUNTER                  | カウンター                       |
| DOCUMENT_CHARSET         | ドキュメントの文字セット              |
| DOCUMENT_REFERRER        | ドキュメントリファラー                 |
| EXTERNAL_REFERRER        | 外部リファラー                   |
| HTML_ATTR                | HTML属性                    |
| SOURCE_URL               | ソースURL                      |
| SOURCE_HOST              | 送信元ホスト                   |
| SOURCE_HOSTNAME          | 送信元ホスト名                 |
| SOURCE_PATH              | ソースパス                       |
| TITLE                    | タイトル                        |
| VIEWER                   | 視聴者                      |
| CONTENT_LOAD_TIME        | コンテンツの読み込み時間            |
| DOMAIN_LOOKUP_TIME       | ドメイン検索時間                |
| DOM_INTERACTIVE_TIME     | DOMインタラクティブタイム              |
| NAV_REDIRECT_COUNT       | ナビゲーションリダイレクトカウント           |
| NAV_TIMING               | ナビゲーションのタイミング               |
| NAV_TYPE                 | ナビゲーションタイプ                  |
| PAGE_DOWNLOAD_TIME       | ページのダウンロード時間              |
| PAGE_LOAD_TIME           | ページ読み込み時間               |
| REDIRECT_TIME            | リダイレクト時間                  |
| SERVER_RESPONSE_TIME     | サーバー応答時間                |
| TCP_CONNECT_TIME         | TCP接続時間                 |
| AVAILABLE_SCREEN_HEIGHT  | 利用可能なスクリーンの高さ          |
| AVAILABLE_SCREEN_WIDTH   | 利用可能な画面幅             |
| BROWSER_LANGUAGE         | ブラウザ言語                    |
| SCREEN_COLOR_DEPTH       | 画面の色深度                 |
| SCREEN_HEIGHT            | スクリーンの高さ                   |
| SCREEN_WIDTH             | スクリーン幅                     |
| SCROLL_HEIGHT            | スクロール高さ                    |
| SCROLL_WIDTH             | スクロール幅                     |
| SCROLL_LEFT              | 左にスクロール                    |
| SCROLL_TOP               | スクロールトップ                    |
| TIMEZONE                 | タイムゾーン                      |
| TIMEZONE_CODE            | タイムゾーンコード                   |
| USER_AGENT               | ユーザーエージェント                  |
| VIEWPORT_HEIGHT          | ビューポートの高さ                  |
| VIEWPORT_WIDTH           | ビューポート幅                    |
| TOTAL_ENGAGED_TIME       | 合計エンゲージメント時間            |
| INCREMENTAL_ENGAGED_TIME | 増分関与時間                |
| \${backgrounded}         | バックグラウンド                    |
| VARIANT                  | バリアント。<amp-experiment>が必要 |
| VARIANTS                 | バリアント。<amp-experiment>が必要 |
| AMP_GEO                  | ジオロケーション。<amp-geo>が必要     |
| AMP_VERSION              | AMPバージョン                    |
| AMP_STATE                | AMPの状態                    |
| BACKGROUND_STATE         | バックグラウンド状態                |
| CLIENT_ID                | クライアントID                    |
| PAGE_VIEW_ID             | ページビューID                    |
| PAGE_VIEW_ID_64          | ページビューID 64                 |
| QUERY_PARAM              | クエリパラメータ                    |
| RANDOM                   | ランダム                        |
| TIMESTAMP                | タイムスタンプ                     |

### 例

#### AMPDOC_HOST

    <amp-pixel src="https://foo.com/pixel?host=AMPDOC_HOST"></amp-pixel>
    # https://foo.com/pixel?host=example.com:8080

#### AMPDOC_HOSTNAME

    <amp-pixel src="https://foo.com/pixel?hostname=AMPDOC_HOSTNAME"></amp-pixel>
    # https://foo.com/pixel?hostname=example.com

#### AMPDOC_URL

    <amp-pixel src="https://foo.com/pixel?ref=AMPDOC_URL"></amp-pixel>
    # https://foo.com/pixel?ref=https%3A%2F%2Fexample.com%2F

#### AMP_STATE

    <amp-pixel src="https://foo.com/pixel?bar=AMP_STATE(foo.bar)"></amp-pixel>

#### AMP_VERSION

    <amp-pixel src="https://foo.com/pixel?v=AMP_VERSION"></amp-pixel>
    # 1460655576651

#### AVAILABLE_SCREEN_HEIGHT

    <amp-pixel src="https://foo.com/pixel?availScreenHeight=AVAILABLE_SCREEN_HEIGHT"></amp-pixel>
    # 1480

#### AVAILABLE_SCREEN_WIDTH

    <amp-pixel src="https://foo.com/pixel?availScreenWidth=AVAILABLE_SCREEN_WIDTH"></amp-pixel>
    # 2500

#### BROWSER_LANGUAGE

    <amp-pixel src="https://foo.com/pixel?lang=BROWSER_LANGUAGE"></amp-pixel>
    # en-us

#### CANONICAL_HOST

    <amp-pixel src="https://foo.com/pixel?host=CANONICAL_HOST"></amp-pixel>
    # http://pinterest.com:9000

#### CANONICAL_HOSTNAME

    <amp-pixel src="https://foo.com/pixel?hostname=CANONICAL_HOSTNAME"></amp-pixel>
    # pinterest.com

#### CANONICAL_PATH

    <amp-pixel src="https://foo.com/pixel?path=CANONICAL_PATH"></amp-pixel>
    # %2Fanalytics.html

#### CANONICAL_URL

    <amp-pixel src="https://foo.com/pixel?href=CANONICAL_URL"></amp-pixel>
    # http%3A%2F%2Fexample.com%3A8000%2Fanalytics.html

#### CLIENT_ID

    <amp-pixel src="https://foo.com/pixel?cid=CLIENT_ID(cid-scope-cookie-fallback-name)"></amp-pixel>
    # U6XEpUs3yaeQyR2DKATQH1pTZ6kg140fvuLbtl5nynbUWtIodJxP5TEIYBic4qcV

#### CONTENT_LOAD_TIME

    <amp-pixel src="https://foo.com/pixel?contentLoadTime=CONTENT_LOAD_TIME"></amp-pixel>
    # 40

#### DOCUMENT_CHARSET

    <amp-pixel src="https://foo.com/pixel?charSet=DOCUMENT_CHARSET"></amp-pixel>
    # UTF-8

#### DOCUMENT_REFERRER

    <amp-pixel src="https://foo.com/pixel?referrer=DOCUMENT_REFERRER"></amp-pixel>
    # https://www.google.com

#### DOMAIN_LOOKUP_TIME

    <amp-pixel src="https://foo.com/pixel?domainLookupTime=DOMAIN_LOOKUP_TIME"></amp-pixel>
    # 1

#### DOM_INTERACTIVE_TIME

    <amp-pixel src="https://foo.com/pixel?domInteractiveTime=DOM_INTERACTIVE_TIME"></amp-pixel>
    # 40

#### EXTERNAL_REFERRER

    <amp-pixel src="https://foo.com/pixel?referrer=EXTERNAL_REFERRER"></amp-pixel>
    # https://www.google.com

#### AMP_GEO

    <amp-pixel src="https://foo.com/pixel?domInteractiveTime=AMP_GEO"></amp-pixel>
    # ca

#### NAV_REDIRECT_COUNT

    <amp-pixel src="https://foo.com/pixel?nrc=NAV_REDIRECT_COUNT"></amp-pixel>
    # 0

#### NAV_TIMING

    <amp-pixel src="https://foo.com/pixel?navStart=NAV_TIMING(navigationStart)&amp;pageLoadTime=NAV_TIMING(navigationStart,loadEventStart)"></amp-pixel>
    # 1451606400000
    # 10

#### NAV_TYPE

    <amp-pixel src="https://foo.com/pixel?nt=NAV_TYPE"></amp-pixel>
    # 1

#### PAGE_DOWNLOAD_TIME

    <amp-pixel src="https://foo.com/pixel?pageDownloadTime=PAGE_DOWNLOAD_TIME"></amp-pixel>
    # 100

#### PAGE_LOAD_TIME

    <amp-pixel src="https://foo.com/pixel?pageLoadTime=PAGE_LOAD_TIME"></amp-pixel>
    # 220

#### PAGE_VIEW_ID

    <amp-pixel src="https://foo.com/pixel?pid=PAGE_VIEW_ID"></amp-pixel>
    # 978

#### PAGE_VIEW_ID_64

    <amp-pixel src="https://foo.com/pixel?pid=PAGE_VIEW_ID_64"></amp-pixel>
    # U6XEpUs3yaeQyR2DKATQH1pTZ6kg140fvuLbtl5nynb

#### QUERY_PARAM

    <amp-pixel src="https://foo.com/pixel?bar=QUERY_PARAM(baz,biz)"></amp-pixel>

#### RANDOM

    <amp-pixel src="https://foo.com/pixel?RANDOM"></amp-pixel>
    # 0.12345632345

#### REDIRECT_TIME

    <amp-pixel src="https://foo.com/pixel?redirectTime=REDIRECT_TIME"></amp-pixel>
    # 0

#### SCREEN_COLOR_DEPTH

    <amp-pixel src="https://foo.com/pixel?colorDepth=SCREEN_COLOR_DEPTH"></amp-pixel>
    # 24

#### SCREEN_HEIGHT

    <amp-pixel src="https://foo.com/pixel?sh=SCREEN_HEIGHT"></amp-pixel>
    # 1600

#### SCREEN_WIDTH

    <amp-pixel src="https://foo.com/pixel?sw=SCREEN_WIDTH"></amp-pixel>
    # 2560

#### SCROLL_HEIGHT

    <amp-pixel src="https://foo.com/pixel?scrollHeight=SCROLL_HEIGHT"></amp-pixel>
    # 400

#### SCROLL_LEFT

    <amp-pixel src="https://foo.com/pixel?scrollLeft=SCROLL_LEFT"></amp-pixel>
    # 100

#### SCROLL_TOP

    <amp-pixel src="https://foo.com/pixel?st=SCROLL_TOP"></amp-pixel>
    # 0

#### SCROLL_WIDTH

    <amp-pixel src="https://foo.com/pixel?scrollWidth=SCROLL_WIDTH"></amp-pixel>
    # 600

#### SERVER_RESPONSE_TIME

    <amp-pixel src="https://foo.com/pixel?serverResponseTime=SERVER_RESPONSE_TIME"></amp-pixel>
    # 10

#### SOURCE_URL

    <amp-pixel src="https://foo.com/pixel?href=SOURCE_URL"></amp-pixel>
    # https://foo.com/pixel?href=https%3A%2F%2Fpinterest.com%2F

#### SOURCE_HOST

    <amp-pixel src="https://foo.com/pixel?host=SOURCE_HOST"></amp-pixel>
    # https://foo.com/pixel?host=pinterest.com:9000

#### SOURCE_HOSTNAME

    <amp-pixel src="https://foo.com/pixel?host=SOURCE_HOSTNAME"></amp-pixel>
    # https://foo.com/pixel?host=pinterest.com

#### SOURCE_PATH

    <amp-pixel src="https://foo.com/pixel?path=SOURCE_PATH"></amp-pixel>
    # https://foo.com/pixel?path=%2Fpage2.html

#### TCP_CONNECT_TIME

    <amp-pixel src="https://foo.com/pixel?tcpConnectTime=TCP_CONNECT_TIME"></amp-pixel>
    # 10

#### TITLE

    <amp-pixel src="https://foo.com/pixel?title=TITLE"></amp-pixel>
    # AMPキュメント

#### TIMESTAMP

    <amp-pixel src="https://foo.com/pixel?timestamp=TIMESTAMP"></amp-pixel>
    # 10

#### TIMEZONE

    <amp-pixel src="https://foo.com/pixel?tz=TIMEZONE"></amp-pixel>
    # 480

#### TIMEZONE_CODE

    <amp-pixel src="https://foo.com/pixel?tz_code=TIMEZONE_CODE"></amp-pixel>
    # Europe/Rome

#### USER_AGENT

    <amp-pixel src="https://foo.com/pixel?sh=USER_AGENT"></amp-pixel>
    # Mozilla/5.0 (Windows NT 6.1; Win64; x64; rv:47.0) Gecko/20100101 Firefox/47.0

#### VIEWER

    <amp-pixel src="https://foo.com/pixel?viewer=VIEWER"></amp-pixel>
    # www.google.com

#### VIEWPORT_HEIGHT

    <amp-pixel src="https://foo.com/pixel?viewportHeight=VIEWPORT_HEIGHT"></amp-pixel>
    # 1600

#### VIEWPORT_WIDTH

    <amp-pixel src="https://foo.com/pixel?viewportHeight=VIEWPORT_HEIGHT"></amp-pixel>
    # 2560
