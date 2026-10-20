# グラフィックエレメント（アーチ）

出典: [グラフィックエレメントとは](https://design-system.isct.ac.jp/ja/brand/elements/graphic-elements/overview/)、
[使用例](https://design-system.isct.ac.jp/ja/brand/elements/graphic-elements/examples/)、
[テキスト表示例](https://design-system.isct.ac.jp/ja/brand/elements/graphic-elements/examples-text/)

## どんなものか

シンボル「Science S」の意味を広げた図形で、**アーチ（ゆるい弧・斜めの帯）**でできている。
公式にはアーチの太さと角度で9種類、表示の仕方9種類が用意されている。色は
ブランドカラーとサブカラー、背景用の拡張色（`#e8eaf1` `#f2f4f9`）。

公式データ（Illustrator / PowerPoint）は学内限定。エージェントが作るときは、公式の形を
写すのではなく、**画面の辺から入る斜めの帯・ゆるい弧**として雰囲気を合わせる。

## 置き方

- 帯は**デザイン領域の4辺のうち3辺以上に接する**ように置く（宙に浮かせない）。
  全面に敷く場合はこの限りでない。
- 背景は白が基本（特殊な紙・素材で色が決まる場合を除く）。
- 帯の上に四角や写真を重ねてよいが、帯の形が分かるよう小さめに。文字量が多いときでも
  覆うのは面積の 70% まで。
- 帯の上に置く四角の色は、白かサブカラー系の背景色。背景色版の帯なら
  ブランドカラー・サブカラーも可。

## 文字を重ねるとき

- 背景色（`#e8eaf1` など）の帯の上の文字は、ブランドカラーか黒が推奨。
- ブランドカラーの太い帯や総柄の上には文字を置かない（背景色版なら可）。
- 帯と文字をくっつけない。背景を文字で埋め尽くさない。

## HTML / SVG で作るときの例

16:9（1920×1080）の表紙。Science Blue の地に、左下からサブカラーの帯、右下に白い楔。
右下の白い部分はロゴ（または大学名テキスト）の置き場所。

```html
<svg width="1920" height="1080" viewBox="0 0 1920 1080" aria-hidden="true">
  <rect width="1920" height="1080" fill="#1c3177"/>
  <polygon points="0,770 1920,1010 1920,1080 0,1080" fill="#7f96c2"/>
  <polygon points="760,1080 1920,860 1920,1080" fill="#ffffff"/>
</svg>
```

中表紙（白地）。上辺から Science Blue の細い楔、下辺にサブカラーの帯。

```html
<svg width="1920" height="1080" viewBox="0 0 1920 1080" aria-hidden="true">
  <rect width="1920" height="1080" fill="#ffffff"/>
  <polygon points="0,0 1920,0 1920,36 0,170" fill="#1c3177"/>
  <polygon points="0,975 1920,1035 1920,1080 0,1080" fill="#7f96c2"/>
</svg>
```

どちらも帯が3辺以上に接している。帯は直線の斜め帯でも、`path` の弧でもよい。
