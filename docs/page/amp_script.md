---
layout: page
---

### 説明

独自の JavaScript を実行

### 使い方

    <amp-script 属性>
    </amp-script>

#### ローカル要素から読み込む

    <head>
      <meta
        name="amp-script-src"
        content="スクリプトハッシュ"/>
    </head>
    <amp-script width="200" height="50" script="ID">
    </amp-script>
    <script id="ID" type="text/plain" target="amp-script">
    </script>

### 必要なスクリプト

    <script async custom-element="amp-script" src="https://cdn.ampproject.org/v0/amp-script-0.1.js"></script>

### 属性

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
| src         | スクリプトURL                                               |
| script      | ローカルスクリプト                                              |
| sandbox     | サンドボックス                                                |
| max-age     | ローカルスクリプトの提供を許可する最大有効期間                      |
| fallback    | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights     | メディア式に基づいた要素の縦サイズ                                 |
| layout      | レイアウト                                                  |
| media       | メディア属性                                               |
| noloading   | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on          | イベントの実行用                                            |
| placeholder | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes       | メディア式に基づいた要素の横サイズ                                 |
| width       | 横幅                                                   |
| height      | 高さ                                                    |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| container    | 子要素に応じて自動的にサイズ調整          |
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整 |
| intrinsic    | 指定したアスペクト比に自動的にサイズ調整       |
| nodisplay    | 要素が非表示                        |
| responsive   | 画面サイズに応じて自動的にサイズ調整         |

### 例

#### 基本的な使い方

    <amp-script
      layout=container
      src="/examples/amp-script/amp-script-demo.js">
      <button id="hello">Insert Hello World!</button>
    </amp-script>

#### ローカルスクリプト

    <amp-script
      script="local-script"
      width=300
      height=20>
      Should say "Hi there!".
    </amp-script>
    <script
      id="local-script"
      type="text/plain"
      target="amp-script">
      document.body.textContent = 'Hi there!';
    </script>

#### サンドボックス(sandbox)

    <amp-script
      sandbox="allow-forms"
      width=300
      height=20
      script="sandbox-allow-forms">
      Should add an input field.
    </amp-script>
    <script
      type="text/plain"
      target="amp-script"
      id="sandbox-allow-forms">
      document.body.appendChild(document.createElement('input'));
    </script>

#### localStorage

    <amp-script
      width=300
      height=40
      script="local-storage"
      sandbox="allow-forms">
      <input id=input type=text>
    </amp-script>
    <script type="text/plain" target="amp-script" id="local-storage">
      const input = document.querySelector('#input');
      const output = document.querySelector('#output');
      const get = document.querySelector('#get');
      const set = document.querySelector('#set');
      const remove = document.querySelector('#remove');
      const clear = document.querySelector('#clear');
      input.addEventListener('change', () => {});
      get.addEventListener('click', () => {
        output.value = input.value ? localStorage.getItem(input.value) : JSON.stringify(localStorage);
      });
      set.addEventListener('click', () => {
        const tuple = input.value.split('=');
        localStorage.setItem(tuple[0], tuple[1]);
      });
      remove.addEventListener('click', () => {
        localStorage.removeItem(input.value);
      });
      clear.addEventListener('click', () => {
        localStorage.clear();
      });
    </script>

#### Canvas

    <amp-script width=300 height=120 src="/examples/amp-script/canvas.js">
      <canvas id="canvas"></canvas>
    </amp-script>

#### amp-state

    <p [text]="bar">Should read "123" after tapping button below.</p>
    <button on="tap: AMP.setState({})">setState()</button>
    <amp-script width=300 height=80 script="bind">
      <pre>AMP.setState({bar: 123})</pre>
      <pre>Prints AMP.getState('foo')</pre>
    </amp-script>
    <script type="text/plain" target="amp-script" id="bind">
      AMP.setState({bar: 123});
      AMP.getState('foo').then(state => console.log(state));
    </script>
    <amp-state id="foo">
      <script type=application/json>
        {
          "bar": "foobar"
        }
      </script>
    </amp-state>
