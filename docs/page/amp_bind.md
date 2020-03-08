---
layout: page
---

### 説明

動的なコンテンツの作成

### 使い方

#### 初期化

    <amp-state id="ID名">
      <script type="application/json">
        {
          初期化したいkeyとvalue
        }
      </script>
    </amp-state>

#### 更新

##### refresh

    <amp-state id="ID名" ...></amp-state>
    <button on="tap:ID名.refresh"></button>

##### AMP.setState

    <button on="tap:AMP.setState({更新したいkeyとvalue})"></button>

##### AMP.setState

    <button on="tap:AMP.pushState({新したいkeyとvalue})"></button>

### 必要なスクリプト

    <script async custom-element="amp-bind" src="https://cdn.ampproject.org/v0/amp-bind-0.1.js"></script>

### 使える JavaScript 関数

#### 配列

| 関数名      | 説明                                                             |
| ----------- | ---------------------------------------------------------------- |
| concat      | 結合                                                             |
| filter      | 条件に一致した要素だけ抽出                                       |
| includes    | 指定した要素が配列に含まれているか                               |
| indexOf     | 指定した要素が配列に含まれている場合にその位置を取得             |
| join        | 配列を結合して文字列に変換                                       |
| lastIndexOf | 指定した要素が配列に含まれているか後ろから検索しその位置を取得   |
| map         | 配列のすべての要素に対して、指定した処理を実行し新しい配列を生成 |
| reduce      | 配列の値を左から右に一つにまとめる                               |
| slice       | 分割                                                             |
| some        | 配列のいずれかの要素が指定した条件を満たしているか               |
| sort        | ソート                                                           |
| splice      | 指定した要素の削除や変更                                         |

#### 数値

| 関数名        | 説明                                               |
| ------------- | -------------------------------------------------- |
| toExponential | 指数形式に変換                                     |
| toFixed       | 小数点以下を指定した桁数で四捨五入して文字列に変換 |
| toPrecision   | 指定した精度で文字列に変換                         |
| toString      | 文字列に変換                                       |

#### 文字列

| 関数名      | 説明                                                         |
| ----------- | ------------------------------------------------------------ |
| charAt      | 指定された位置の文字を取得                                   |
| charCodeAt  | UTF-16に変換                                                |
| concat      | 結合                                                         |
| indexOf     | 指定した文字で検索し、初めに現れたインデックスを取得         |
| lastIndexOf | 指定した文字で後ろから検索し、初めに現れたインデックスを取得 |
| slice       | 文字列の一部を取り出す                                       |
| split       | 指定した区切り文字で分割して配列を作成                       |
| substr      | 開始位置から文字数分の部分文字列を取り出す                   |
| substring   | 指定された範囲の文字列を取り出す                             |
| toLowerCase | ローワーキャメルケース変換                                   |
| toUpperCase | アッパーキャメルケース変換                                   |

#### 計算

| 関数名 | 説明                             |
| ------ | -------------------------------- |
| abs    | 数値の絶対値を取得               |
| ceil   | 指定した値以上で最小の整数を取得 |
| floor  | 指定した値以下で最大の整数を取得 |
| max    | 最大値                           |
| min    | 最小値                           |
| random | ランダム                         |
| round  | 四捨五入                         |
| sign   | 正数、ゼロ、負数を判定           |

#### オブジェクト

| 関数名 | 説明           |
| ------ | -------------- |
| keys   | キー名を取得   |
| values | バリューを取得 |

#### グローバル

| 関数名             | 説明                 |
| ------------------ | -------------------- |
| encodeURI          | URLエンコード       |
| encodeURIComponent | UTF-8文字エンコード |

### バインドが使える属性

| タグ名                     | 属性                                                                                                                                                                                                                                                                                            |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| amp-brightcove             | \[data-account\] \[data-embed\] \[data-player\] \[data-player-id\] \[data-playlist-id\] \[data-video-id\]                                                                                                                                                                                       |
| amp-carousel type="slides" | \[slide\]\*                                                                                                                                                                                                                                                                                     |
| amp-date-picker            | \[min\] \[max\]                                                                                                                                                                                                                                                                                 |
| amp-google-document-embed  | \[src\] \[title\]                                                                                                                                                                                                                                                                               |
| amp-iframe                 | \[src\]                                                                                                                                                                                                                                                                                         |
| amp-img                    | \[alt\] \[attribution\] \[src\] \[srcset\]                                                                                                                                                                                                                                                      |
| amp-lightbox               | \[open\]\*                                                                                                                                                                                                                                                                                      |
| amp-list                   | \[src\]                                                                                                                                                                                                                                                                                         |
| amp-selector               | \[selected\]\* \[disabled\]                                                                                                                                                                                                                                                                     |
| amp-state                  | \[src\]                                                                                                                                                                                                                                                                                         |
| amp-video                  | \[alt\] \[attribution\] \[controls\] \[loop\] \[poster\] \[preload\] \[src\]                                                                                                                                                                                                                    |
| amp-youtube                | \[data-videoid\]                                                                                                                                                                                                                                                                                |
| a                          | \[href\]                                                                                                                                                                                                                                                                                        |
| button                     | \[disabled\] \[type\] \[value\]                                                                                                                                                                                                                                                                 |
| details                    | \[open\]                                                                                                                                                                                                                                                                                        |
| fieldset                   | \[disabled\]                                                                                                                                                                                                                                                                                    |
| image                      | \[xlink:href\]                                                                                                                                                                                                                                                                                  |
| input                      | \[accept\] \[accessKey\] \[autocomplete\] \[checked\] \[disabled\] \[height\] \[inputmode\] \[max\] \[maxlength\] \[min\] \[minlength\] \[multiple\] \[pattern\] \[placeholder\] \[readonly\] \[required\] \[selectiondirection\] \[size\] \[spellcheck\] \[step\] \[type\] \[value\] \[width\] |
| option                     | \[disabled\] \[label\] \[selected\] \[value\]                                                                                                                                                                                                                                                   |
| optgroup                   | \[disabled\] \[label\]                                                                                                                                                                                                                                                                          |
| select                     | \[autofocus\] \[disabled\] \[multiple\] \[required\] \[size\]                                                                                                                                                                                                                                   |
| source                     | \[src\] \[type\]                                                                                                                                                                                                                                                                                |
| track                      | \[label\] \[src\] \[srclang\]                                                                                                                                                                                                                                                                   |
| textarea                   | \[autocomplete\] \[autofocus\] \[cols\] \[disabled\] \[maxlength\] \[minlength\] \[placeholder\] \[readonly\] \[required\] \[rows\] \[selectiondirection\] \[selectionend\] \[selectionstart\] \[spellcheck\] \[wrap\]                                                                          |

### 例

#### 基本的な使い方

    <p [text]="foo">After clicking the button below, this will read 'foo'<p>
    <p id="foo" [text]="foo + 'bar'">And this will read 'foobar'<p>
    <p [text]="myState.myStateKey1">This will read 'myStateValue1'<p>
    <button [disabled]="isButtonDisabled">This button will be disabled</button>
    <p [class]="textClass">This text will have have a red background color</p>
    <amp-img src="https://amp.dev/static/samples/img/Border_Collie.jpg" [src]="imgSrc" width=100 [width]="imgSize || 100" height=100 [height]="imgSize || 100" alt="asdf" [alt]="imgAlt" [aria-label]="'Image of a ' + imgAlt"></amp-img>
    <p>The image above will increase in size and change its src</p>
    <div>
      <button on="tap:AMP.setState({'foo': 'foo', 'isButtonDisabled': true, 'textClass': 'redBackground', 'imgSrc': 'https://amp.dev/static/samples/img/Shetland_Sheepdog.jpg', 'imgSize': 200, 'imgAlt': 'Sheepdog'})">Click me</button>
    </div>
    <amp-state id="myState">
      <script type="application/json">
        {
          "myStateKey1": "myStateValue1"
        }
      </script>
    </amp-state>

#### カルーセルの画像を選択して文字を変更

    <p [text]="'Selected slide: ' + selectedSlide">Selected slide: None<p>
    <amp-carousel controls type=slides width=400 height=300
      [slide]="selectedSlide" on="slideChange:AMP.setState({selectedSlide: event.index})">
      <amp-img src="https://amp.dev/static/samples/img/image1.jpg" width=400 height=300></amp-img>
      <amp-img src="https://amp.dev/static/samples/img/image2.jpg" width=400 height=300></amp-img>
    </amp-carousel>

#### カルーセルの画像をクリックしたら選択済みに変更

    <amp-carousel controls width=400 height=100>
      <amp-img src="https://amp.dev/static/samples/img/image1.jpg" width=100 height=75
        [class]="selectedSlide == 0 ? 'selected' : ''" on="tap:AMP.setState({selectedSlide: 0})"></amp-img>
      <amp-img src="https://amp.dev/static/samples/img/image2.jpg" width=100 height=75
        [class]="selectedSlide == 1 ? 'selected' : ''" on="tap:AMP.setState({selectedSlide: 1})"></amp-img>
    </amp-carousel>

#### ボタンでカルーセルの画像を切り替える

    <button on="tap:AMP.setState({selectorDisabled: !selectorDisabled})">Toggle selector[disabled]</button>
    <amp-selector layout=container name="carousel-selector" [selected]="selectedSlide"
      on="select:AMP.setState({selectedSlide: event.targetOption})"
      [disabled]="selectorDisabled">
      <amp-carousel controls width=400 height=100>
        <amp-img src="https://amp.dev/static/samples/img/image1.jpg" width=100 height=75 option=0></amp-img>
        <amp-img src="https://amp.dev/static/samples/img/image2.jpg" width=100 height=75 option=1></amp-img>
      </amp-carousel>
    </amp-selector>

#### ボタンをクリックしたら表示(details)

    <amp-state id="detailsOpen">false</amp-state>
    <button on="tap:AMP.setState({ detailsOpen: ! detailsOpen })" [text]="detailsOpen ? 'Toggle Closed' : 'Toggle Open'">Toggle Open</button>
    <details [open]="detailsOpen">
      <summary>Learn more</summary>
      <p>This is more information.</p>
    </details>

#### Form

    <button on="tap:AMP.setState({selected: 1})">1</button>
    <button on="tap:AMP.setState({selected: 2})">2</button>
    <button on="tap:AMP.setState({selected: 3})">3</button>
    <button on="tap:AMP.setState({selected: 4})">4</button>
    <p [text]="'$' + selectedRange">$0</p>
    <p>Color Selection: <span [text]="colorSelection || 'red'">red</span>
    <button on="tap:AMP.setState({nameVar: 'Alice', emailVar: 'alice@fake.com'}), myForm.submit">
      Set name/email with amp-bind and submit (chained action)
    </button>
    <form method="post"
      action-xhr="/form/echo-json/post"
      target="_blank"
      id="myForm">
      <fieldset>
        <label>
          <span>Your name</span>
          <input type="text" name="name" id="name1" [value]="nameVar" required>
        </label>
        <label>
          <span>Your email</span>
          <input type="email" name="email" id="email1" [value]="emailVar" required>
        </label>
        <label>
          <span>Your choice</span>
          <select on="change:AMP.setState({colorSelection: event.value})">
            <option value="red">red</option>
            <option value="green">green</option>
            <option value="blue">blue</option>
            <option value="yellow">yellow</option>
          </select>
        </label>
        <label>
          <span>Your offer</span>
          $100
          <input type="range" min="100" max="200" step="10" on="change:AMP.setState({selectedRange: event.value})"/>
          $200
        </label>
        <input type="submit" value="Subscribe">
      </fieldset>
      <div submit-success>
        <template type="amp-mustache">
          Success! Thanks {{name}} for entering your email: {{email}}
          <p>You have selected: <span [text]="selected ? selected : 'No selection'">No selection</span></p>
        </template>
      </div>
      <div submit-error>
        <template type="amp-mustache">
          Error! Failure to register: {{name}} : {{email}}
          <p>You have selected: <span [text]="selected ? selected : 'No selection'">No selection</span></p>
        </template>
      </div>
    </form>

#### iframe

    <button on="tap:AMP.setState({bling: 'https://giphy.com/embed/DKG1OhBUmxL4Q'})">Change iframe src</button>
    <amp-iframe width="500" height="281"
      sandbox="allow-scripts allow-same-origin allow-popups" allowfullscreen frameborder="0"
      src="https://player.vimeo.com/video/140261016" [src]="bling">
    </amp-iframe>

#### URLを指定してリスト更新(amp-list)

    <button on="tap:AMP.setState({src:'/list/fruit-data/get'})">Show Fruit</button>
    <template id="my-template" type="amp-mustache">
      <strong>name</strong> {{name}}
    </template>
    <amp-list layout="responsive" src="/list/fruit-data/get" [src]="src || '/list/fruit-data/get'" width="600" height="100" template="my-template">
      <div placeholder>(Placeholder)</div>
    </amp-list>

#### JSONを指定してリスト更新(amp-list)

    <amp-state id="otherFoods">
      <script type="application/json">
        [{
          "name": "pizza"
        }, {
          "name": "ice cream"
        }]
      </script>
    </amp-state>
    <button on="tap:AMP.setState({src: otherFoods})">Show Other Foods</button>
    <template id="my-template" type="amp-mustache">
      <strong>name</strong> {{name}}
    </template>
    <amp-list layout="responsive" src="/list/fruit-data/get" [src]="src || '/list/fruit-data/get'" width="600" height="100" template="my-template">
      <div placeholder>(Placeholder)</div>
    </amp-list>

#### ボタンをクリックして指定したJSONで更新

    <button on="tap:AMP.setState({
      src: [{
        name: 'pizza'
      }, {
        name: 'burger'
      }]
    })">Show Junk Food</button>
    <template id="my-template" type="amp-mustache">
      <strong>name</strong> {{name}}
    </template>
    <amp-list layout="responsive" src="/list/fruit-data/get" [src]="src || '/list/fruit-data/get'" width="600" height="100" template="my-template">
      <div placeholder>(Placeholder)</div>
    </amp-list>

#### live-list

    <button on="tap:AMP.setState({favoriteFood: 'pizza'})">Pizza</button>
    <button on="tap:AMP.setState({favoriteFood: 'pasta'})">Pasta</button>
    <button on="tap:AMP.setState({favoriteFood: 'cake'})">Cake</button>
    <amp-live-list
      layout="container"
      data-poll-interval="15000"
      data-max-items-per-page="5"
      id="live-blog-1">
      <button id="live-list-update-button" update class="button"
        on="tap:live-blog-1.update">You have updates</button>
      <div items>
        <div id="live-blog-item-1" data-sort-time="1466669033418">
          <h3 class="headline">
            <a href="#live-blog-item-1">Bacon ipsum dolor amet</a>
          </h3>
          <div class="article-body">
            As you can see, bacon is far superior to <b><span [text]='favoriteFood'>everything!</span></b>!
          </div>
        </div>
      </div>
    </amp-live-list>

#### amp-bind-macro

    <amp-bind-macro id="add" expression="a + b" arguments="a, b"></amp-bind-macro>
    <p [text]="three || '1 + 2 = ?'">1 + 2 = ?</p>
    <button on="tap:AMP.setState({three: add(1, 2)})">Compute</button>

#### svgimage

    <svg height="500" width="500">
      <image xlink:href="https://amp.dev/static/samples/img/Border_Collie.jpg" [xlink:href]='href'></image>
    </svg>
    <button on="tap:AMP.setState({'href': 'https://amp.dev/static/samples/img/Shetland_Sheepdog.jpg'})">update image</button>

#### ボタンでYouTubeを切り替える

    <amp-youtube width=480 height=270 data-videoid="lBTCB7yLs8Y"
      [data-videoid]="youtubeId || 'lBTCB7yLs8Y'">
    </amp-youtube>
    <p>
      <button on="tap:AMP.setState({
        youtubeId: 'WrpkFROqR0Q'
      })">Change amp-youtube</button>
    </p>

#### 条件で出力する文字を変更

    <p [text]="charState">
      Try typing a few characters into the textbox.
    </p>
    <input type="textbox"
      on="input-throttled:AMP.setState({
        charState: event.value.length < 10 ?
        'There are under 10 characters, type more!' :
        'You
      })">
