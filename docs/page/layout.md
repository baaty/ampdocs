---
layout: page
---

### 属性

| 属性名      | 説明                                                     |
| ----------- | -------------------------------------------------------- |
| width       | 横幅                                                     |
| height      | 高さ                                                     |
| layout      | レイアウト                                               |
| sizes       | メディア式に基づいた要素の横サイズ                       |
| heights     | メディア式に基づいた要素の縦サイズ                       |
| media       | メディア属性                                             |
| placeholder | プレスホルダー                                           |
| fallback    | フォールバック                                           |
| noloading   | 進捗インジケータ(グルグル回るアイコンみたいなやつ)をOFF |

### layout 属性で指定できる値

| 値           | 説明                                             |
| ------------ | ------------------------------------------------ |
| container    | 子要素に応じて自動的にサイズ調整                 |
| fill         | 利用可能なスペースを埋めるよう自動的にサイズ調整 |
| fixed        | 指定した横幅と高さで固定                         |
| fixed-height | 指定した高さで固定。横幅は自動的にサイズ調整     |
| flex-item    | 親要素や周りの要素に応じて自動的にサイズ調整     |
| intrinsic    | 指定したアスペクト比に自動的にサイズ調整         |
| nodisplay    | 要素が非表示                                     |
| responsive   | 画面サイズに応じて自動的にサイズ調整             |

### layout 属性が設定されていない場合

| 条件                                                          | 値           |
| ------------------------------------------------------------- | ------------ |
| heightが指定、widthが指定されていない、もしくはautoが指定 | fixed-height |
| widthが指定、sizes属性が指定                                | responsive   |
| widthが指定、sizes属性が指定されていない                    | fixed        |
| widthとheightの両方が指定されていない                      | container    |