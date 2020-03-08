---
layout: page
---

### 説明

サイドバーを表示

### 使い方

    <amp-sidebar 属性>
    </amp-sidebar>

### 必要なスクリプト

    <script async custom-element="amp-sidebar" src="https://cdn.ampproject.org/v0/amp-sidebar-0.1.js"></script>

### 属性

| 属性名                       | 説明                                                   |
|------------------------------|--------------------------------------------------------|
| layout(必須)                 | レイアウト                                                  |
| side                         | ページのどちら側からサイドバーを開くのかを指定                            |
| open                         | サイドバーが開いているときに存在                                    |
| data-close-button-aria-label | 閉じるボタンのARIAラベル                                        |
| toolbar                      | ツールバーを表示                                             |
| toolbar-target               | 指定IDにツールバーを配置                                      |
| fallback                     | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights                      | メディア式に基づいた要素の縦サイズ                                 |
| media                        | メディア属性                                               |
| noloading                    | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on                           | イベントの実行用                                            |
| placeholder                  | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes                        | メディア式に基づいた要素の横サイズ                                 |
| width                        | 横幅                                                   |
| height                       | 高さ                                                    |

### アクション

| アクション名 | 説明       |
|---------|-----------|
| open    | サイドバーを開く  |
| close   | サイドバーを閉じる |

toggle ｜サイドバーの状態を切り替る

### レイアウト

| レイアウト名   | 説明        |
|-----------|-----------|
| nodisplay | 要素が非表示 |

### ルール

- amp-sidebarは、bodyの直接の子
- サイドバーを表示できるのは、ページの左側または右側
- サイドバーの最大高さは100vh。超えた場合は垂直スクロールバーが表示

### 例

#### 基本的な使い方

    <amp-sidebar id="sidebar1" layout="nodisplay" side="right">
      <ul>
        <li>Nav item 1</li>
        <li><a href="#idTwo" on="tap:idTwo.scrollTo">Nav item 2</a></li>
      </ul>
    </amp-sidebar>

#### ツールバー

    <amp-sidebar id="sidebar1" layout="nodisplay" side="right">
      <ul>
        <li>Nav item 1</li>
        <li><a href="#idTwo" on="tap:idTwo.scrollTo">Nav item 2</a></li>
      </ul>
      <nav toolbar="(max-width: 767px)" toolbar-target="target-element">
        <ul>
          <li>
            <input placeholder="Search..."/>
          </li>
        </ul>
      </nav>
    </amp-sidebar>
    <div id="target-element">
    </div>
