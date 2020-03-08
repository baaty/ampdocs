---
layout: page
---

### 説明

高機能な入力フォームを表示

### 使い方

    <amp-form 属性>
    </amp-form>

### 必要なスクリプト

    <script async custom-element="amp-form" src="https://cdn.ampproject.org/v0/amp-form-0.1.js"></script>

### 属性

| 属性名                      | 説明                                                   |
|-----------------------------|--------------------------------------------------------|
| target                      | フォームの送信後に回答を表示する場所                            |
| action                      | フォームの入力を処理するサーバのURL                                |
| action-xhr(POST の場合は必須) | フォームの入力を処理し、XMLHttpRequestで送信するサーバーのURL          |
| accept-charset              | サーバが使える文字エンコーディングのリスト                               |
| autocomplete                | ブラウザーによる値の入力補完を受けるか                              |
| enctype                     | コンテンツのMIMEタイプ                                          |
| method                      | HTTPメソッド                                               |
| name                        | フォームの名前                                              |
| novalidate                  | 送信するときに検証しない                                       |
| fallback                    | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                     | メディア式に基づいた要素の縦サイズ                                 |
| layout                      | レイアウト                                                  |
| media                       | メディア属性                                               |
| noloading                   | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                          | イベントの実行用                                            |
| placeholder                 | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                       | メディア式に基づいた要素の横サイズ                                 |
| width                       | 横幅                                                   |
| height                      | 高さ                                                    |

### 例

#### 基本的な使い方

    <form method="post" action-xhr="/form/echo-json/post" target="_blank">
      <textarea name="textarea-ctrl-submit">Press Ctrl+Enter to submit this text</textarea><br>
      <input name="submit-button" type="submit" value="Submit" />
      <div submit-success>
        <template type="amp-mustache">
          Success! {{textarea-ctrl-submit}}
        </template>
      </div>
    </form>

#### GET

    <form method="get" action="/form/search-html/get" target="_blank">
      <fieldset>
        <label>
          <span>Search for</span>
          <input type="search" name="term" required>
        </label>
        <input name="submit-button" type="submit" value="Search">
      </fieldset>
    </form>

#### Bind

    <amp-state id="ampBindStateGetNonXhrSameOrigin">
      <script type="application/json">
        "Not Changed"
      </script>
    </amp-state>
    <form id="amp-bind-form-get-non-xhr-same-origin" method="get" action="/form/search-html/get" target="_blank">
      <fieldset>
        <input name="clientId" type="hidden" value="CLIENT_ID(poll)" data-amp-replace="CLIENT_ID">
        <input name="canonicalUrl" type="hidden" value="RANDOM and CANONICAL_URL" data-amp-replace="CANONICAL_URL RANDOM">
        <label>
          <span>Search for</span>
          <input type="search" name="term" required>
        </label>
        <input hidden type="text" name="ampBind" [value]="ampBindStateGetNonXhrSameOrigin">
      </fieldset>
      <button type="button" on="tap:AMP.setState({ ampBindStateGetNonXhrSameOrigin: 'Changed Amp Bind State for ampBindStateGetNonXhrSameOrigin' }), amp-bind-form-get-non-xhr-same-origin.submit">
        Submit AMP Bind Search
      </button>
    </form>

#### events

    <div id="msg">This message will hide when the form is submitted</div>
    <form method="post"
      action-xhr="/form/echo-json/post"
      target="_blank"
      on="submit:msg.hide;submit-success:success-lightbox;submit-error:error-lightbox">
      <fieldset>
        <label>
            <span>Your name</span>
            <input type="text" name="name" id="name3" required>
        </label>
        <label>
            <span>Your email</span>
            <input type="email" name="email" id="email3" required>
        </label>
        <input name="submit-button" type="submit" value="Subscribe">
      </fieldset>
      <div class="form-message invalid-message">
        There are some input that needs fixing. Please fix them.
      </div>
      <div class="form-message valid-message">
        Everything looks good, you can submit now!
      </div>
      <div class="form-message submitting-message">
        Please hold on while we submit your answer!
      </div>
      <div submit-success>
        <template type="amp-mustache">
          Success! Thanks {{name}} for subscribing! Please make sure to check your email {{email}}
          to confirm!
        </template>
      </div>
      <div submit-error>
        <template type="amp-mustache">
          Oops! {{name}}, We apologies something went wrong. Please try again later.
        </template>
      </div>
    </form>
