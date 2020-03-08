---
layout: page
---

### 説明

タップするとネストされたサブメニューを開くメニューを表示

### 使い方

    <amp-nested-menu 属性>
    </amp-nested-menu>

### 必要なスクリプト

    <script async custom-element="amp-nested-menu" src="https://cdn.ampproject.org/v0/amp-nested-menu-0.1.js"></script>
    <script async custom-element="amp-sidebar" src="https://cdn.ampproject.org/v0/amp-sidebar-0.1.js"></script>

### 属性

| 属性名      | 説明                                                   |
|-------------|--------------------------------------------------------|
| side        | サブメニューがどちら側から開くか                                     |
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

### アクション

| アクション名 | 説明                             |
|---------|--------------------------------|
| reset   | 開いているサブメニューをすべて閉じて、ルートメニューに戻る |

### レイアウト

| レイアウト名 | 説明                               |
|---------|----------------------------------|
| fill    | 利用可能なスペースを埋めるよう自動的にサイズ調整 |

### 例

#### 基本的な使い方

    <amp-sidebar layout="nodisplay">
      <amp-nested-menu layout="fill" side="left">
        <ul>
          <li>
            <div amp-nested-submenu-open>open submenu 1</div>
            <div amp-nested-submenu>
              <div amp-nested-submenu-close>close submenu 1</div>
              <amp-img layout="fill" src="img"></amp-img>
            </div>
          </li>
          <li>
            <h2 amp-nested-submenu-open>open submenu 2</h2>
            <div amp-nested-submenu>
              <h2 amp-nested-submenu-close>close submenu 2</h2>
              <amp-accordion></amp-accordion>
            </div>
          </li>
        </ul>
      </amp-nested-menu>
    </amp-sidebar>

#### dynamic template

    <amp-sidebar layout="nodisplay">
      <amp-list layout="fill" src="list" single-item>
        <template type="amp-mustache">
          <amp-nested-menu layout="fill">
            \{\{#items\}\}
            <div>
              <h4 amp-nested-submenu-open>\{\{name\}\}</h4>
              <div amp-nested-submenu>
                <button amp-nested-submenu-close>back</button>
                <a href="\{\{link\}\}">link</a>
              </div>
            </div>
            \{\{/items\}\}
          </amp-nested-menu>
        </template>
      </amp-list>
    </amp-sidebar>
