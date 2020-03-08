---
layout: page
---

### 説明

iframeを作成しGitHubからGistを表示

### 使い方

    <amp-gist 属性>
    </amp-gist>

### 必要なスクリプト

    <script async custom-element="amp-gist" src="https://cdn.ampproject.org/v0/amp-gist-0.1.js"></script>

### 属性

| 属性名           | 説明                                                   |
|------------------|--------------------------------------------------------|
| data-gfyid(必須) | gist ID                                                |
| layout(必須)     | レイアウト                                                  |
| height(必須)     | 高さ                                                    |
| data-file        | データファイル                                                |
| fallback         | フォールバック。対象の要素にブラウザが未対応や読み込みに失敗などをユーザに伝えるもの |
| heights          | メディア式に基づいた要素の縦サイズ                                 |
| layout           | レイアウト                                                  |
| media            | メディア属性                                               |
| noloading        | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF                      |
| on               | イベントの実行用                                            |
| placeholder      | 親要素のプレスホルダー(アニメーションや画像などで読み込まれる前に表示されるやつ)    |
| sizes            | メディア式に基づいた要素の横サイズ                                 |
| width            | 横幅                                                   |
| height           | 高さ                                                    |

### レイアウト

| レイアウト名      | 説明                               |
|--------------|----------------------------------|
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整 |

### 例

#### 基本的な使い方

    <amp-gist
      layout="fixed-height"
      height="241"
      data-gistid="b9bb35bc68df68259af94430f012425f">
    </amp-gist>

#### データファイル(data-file)

    <amp-gist
      data-file="hi.c"
      layout="fixed-height"
      height="197"
      data-gistid="a19e811dcd7df10c4da0931641538497">
    </amp-gist>
