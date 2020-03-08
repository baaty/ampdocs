---
layout: page
---

### 説明

クリック時にコンテンツを開閉するメニューを表示

### 使い方

    <amp-mega-menu 属性>
    </amp-mega-menu>

### 必要なスクリプト

    <script async custom-element="amp-mega-menu" src="https://cdn.ampproject.org/v0/amp-mega-menu-0.1.js"></script>

### 属性

| 属性名                       | 説明                                                   |
|------------------------------|--------------------------------------------------------|
| data-close-button-aria-label | 閉じるボタンのARIAラベルを設定                                   |
| fallback                     | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                      | メディア式に基づいた要素の縦サイズ                                 |
| layout                       | レイアウト                                                  |
| media                        | メディア属性                                               |
| noloading                    | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                           | イベントの実行用                                            |
| placeholder                  | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                        | メディア式に基づいた要素の横サイズ                                 |
| width                        | 横幅                                                   |
| height                       | 高さ                                                    |

### 含められるタグ

- \<h1\>、\<h2\>、\<h3\>、\<h4\>、\<h5\>、\<h6\>
- \<a\>
- \<button\>
- \<span\>
- \<div\>

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |

### 例

#### 基本的な使い方

    <amp-mega-menu layout="fixed-height" height="80">
      <nav>
        <ul>
          <li>
            <button>item</button>
            <div role="dialog">
              <ul>
                <li><div role="menu"></div></li>
              </ul>
            </div>
          </li>
          <li>
            <a>link</a>
          </li>
        </ul>
      </nav>
    </amp-mega-menu>

#### テンプレートあり(template)

    <amp-mega-menu layout="fixed-height" height="80">
      <amp-list layout="fill" src=".">
        <template type="amp-mustache">
          <nav>
            <ul>
              {{items}}
              <li>
                <div role="button">{{name}}</div>
                <div role="dialog"></div>
              </li>
              {{items}}
            </ul>
          </nav>
        </template>
      </amp-list>
    </amp-mega-menu>
