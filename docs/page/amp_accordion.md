---
layout: page
---

### 説明

クリックして開閉するアコーディオン型メニューを表示

### 使い方

    <amp-accordion [属性]>
        <section>
        </section>

        <section>
        </section>
    </amp-accordion>

### 必要なスクリプト

    <script async custom-element="amp-accordion" src="https://cdn.ampproject.org/v0/amp-accordion-0.1.js"></script>

### 属性

| 属性名                 | 説明                                                   |
|------------------------|--------------------------------------------------------|
| animate                | 開閉動作をアニメーション化                                     |
| disable-session-states | 開閉状態を保持しない                                       |
| expanded               | sectionに対して設定するとページ読み込み時に展開した状態              |
| expand-single-section  | 一度に一つのsetionだけが展開                                 |
| data-\*                | data属性                                               |
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

### イベント

| イベント名   | 説明                          |
|----------|-----------------------------|
| expand   | 折りたたみ状態から展開状態に変化する時 |
| collapse | 展開状態から折りたたみ状態に変化する時 |

### アクション

| アクション名  | 説明             |
|----------|----------------|
| expand   | 折りたたみ状態から展開 |
| toggle   | 開閉状態の切り替え  |
| collapse | 展開状態から折りたたみ |

### レイアウト

| レイアウト名   | 説明                      |
|-----------|-------------------------|
| container | 子要素に応じて自動的にサイズ調整 |

### ルール

- amp-accordionの直接の子要素は、section要素のみ
- sectionは、必ず2つの子要素が必要
- sectionの1つ目の子要素は開閉ボタン。見出し要素(h1、h2、h3、h4、h5、h6、header)のみ
- sectionの2つ目の子要素は内容。任意のタグの指定が可能

### 例

#### アコーディオンを表示

    <amp-accordion disable-session-states>
      <section>
        <h2>Section 1</h2>
        <p>Content in section 1.</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Content in section 2.</div>
      </section>
      <section expanded>
        <h2>Section 3</h2>
        <amp-img src="/static/inline-examples/images/squirrel.jpg" width="320" height="256"></amp-img>
      </section>
    </amp-accordion>

#### 開閉をアニメーション化

    <amp-accordion animate>
      <section>
        <h2>Section 1</h2>
        <p>Content in section 1.</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Content in section 2.</div>
      </section>
    </amp-accordion>

#### 開閉状態を保持しない

    <amp-accordion id="my-accordion"{\% if not format=='email'\%} disable-session-states{\% endif \%}>
      <section>
        <h2>Section 1</h2>
        <p>Content in section 1.</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Content in section 2.</div>
      </section>
    </amp-accordion>

#### ページ読み込み時に展開した状態

    <amp-accordion disable-session-states>
      <section expanded>
        <h2>Section 1</h2>
        <p>Content in section 1.</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Content in section 2.</div>
      </section>
    </amp-accordion>

#### 一度に一つのsetionだけが展開

    <amp-accordion expand-single-section>
      <section>
        <h2>Section 1</h2>
        <p>Content in section 1.</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Content in section 2.</div>
      </section>
    </amp-accordion>

#### 開くボタン・閉じるボタンを使って開閉(data属性使用)

    <amp-accordion>
      <section [data-expand]="sectionOne" on="expand:AMP.setState({sectionOne: true});collapse:AMP.setState({sectionOne: false})">
        <h2>Section 1</h2>
        <p>Bunch of awesome content</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Bunch of awesome content</div>
      </section>
    </amp-accordion>
    <button on="tap:AMP.setState({sectionOne: true})">Expand section 1</button>
    <button on="tap:AMP.setState({sectionOne: false})">Collapse section 1</button>

#### ボタンを使って全開閉(toggle)

    <amp-accordion id="myAccordion">
      <section id="section1">
        <h2>Section 1</h2>
        <p>Bunch of awesome content</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Bunch of awesome content</div>
      </section>
    </amp-accordion>
    <button on="tap:myAccordion.toggle">Toggle All Sections</button>

#### ボタンを使って指定したsectionの開閉(toggle)

    <amp-accordion id="myAccordion">
      <section id="section1">
        <h2>Section 1</h2>
        <p>Bunch of awesome content</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Bunch of awesome content</div>
      </section>
    </amp-accordion>
    <button on="tap:myAccordion.toggle(section='section1')">Toggle Section 1</button>

#### ボタンを使って全て展開(expand)

    <amp-accordion id="myAccordion">
      <section id="section1">
        <h2>Section 1</h2>
        <p>Bunch of awesome content</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Bunch of awesome content</div>
      </section>
    </amp-accordion>
    <button on="tap:myAccordion.expand">Expand All Sections</button>

#### ボタンを使って指定したsectionを展開(expand)

    <amp-accordion id="myAccordion">
      <section id="section1">
        <h2>Section 1</h2>
        <p>Bunch of awesome content</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Bunch of awesome content</div>
      </section>
    </amp-accordion>
    <button on="tap:myAccordion.expand(section='section1')">Expand Section 1</button>

#### ボタンを使って全て閉じる(collapse)

    <amp-accordion id="myAccordion">
      <section id="section1">
        <h2>Section 1</h2>
        <p>Bunch of awesome content</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Bunch of awesome content</div>
      </section>
    </amp-accordion>
    <button on="tap:myAccordion.collapse">Collapse All Sections</button>

#### ボタンを使って指定したsectionを閉じる(collapse)

    <amp-accordion id="myAccordion">
      <section id="section1">
        <h2>Section 1</h2>
        <p>Bunch of awesome content</p>
      </section>
      <section>
        <h2>Section 2</h2>
        <div>Bunch of awesome content</div>
      </section>
    </amp-accordion>
    <button on="tap:myAccordion.collapse(section='section1')">Collapse Section 1</button>

#### sectionを連動

    <amp-accordion id="myAccordion">
      <section id="section1" on="expand:myAccordion.expand(section='section2')">
        <h2>Section 1</h2>
        <p>Opening me will open Section 2</p>
      </section>
      <section id="section2" on="collapse:myAccordion.collapse(section='section1')">
         <h2>Section 2</h2>
         <div>Closing me will close Section 1</div>
      </section>
    </amp-accordion>

#### 背景を変える(CSS)

    amp-accordion {
      background-color：green;
    }
