# 書体

出典: [タイポグラフィ](https://design-system.isct.ac.jp/ja/brand/elements/typography/)、
[パワーポイントテンプレート](https://design-system.isct.ac.jp/ja/application/powerpoint-templates/)

## 推奨書体

| 場面 | 和文 | 欧文 |
|---|---|---|
| Web、Illustrator などの制作物、HTML スライド | Noto Sans JP | Hind |
| PowerPoint・Word などオフィス文書（公式テンプレートも同じ） | 游ゴシック（Medium 以上） | 游ゴシック |

- 和文の中に出てくる英数字は Noto Sans JP のまま組む（Hind に切り替えない）。
- 英語だけの要素（英文の文献リスト、英語の大学名・組織名、英語のスライド）は Hind。
- 游ゴシックは Regular だと細く見えるので Medium 以上を使う。

## Web / HTML での読み込み

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&display=swap">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Hind:wght@400;500;600;700&display=swap">
```

```css
body { font-family: 'Noto Sans JP', 'Yu Gothic Medium', 'YuGothic', sans-serif; }
.en  { font-family: 'Hind', 'Noto Sans JP', sans-serif; }
```

## 文字サイズの目安（公式の規定ではなく、このスキルの推奨）

16:9・1920×1080 px のスライド:

| 役割 | サイズ | 太さ | 色 |
|---|---|---|---|
| 表紙タイトル | 84–96 px | 700 | 白（Science Blue 背景） |
| スライド見出し | 60–64 px | 700 | `#1c3177` |
| 小見出し（アイブロウ） | 26 px | 700 | `#435ea5` |
| 本文 | 26–32 px | 400–500 | `#333333` |
| 注記・フッター | 24 px | 400 | `#595959` |

A4 文書: 本文 10.5–11 pt、見出し 13–16 pt（Science Blue、太字）、行間 1.5 前後。
