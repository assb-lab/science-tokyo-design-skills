---
name: science-tokyo-design
description: Apply the Institute of Science Tokyo (東京科学大学 / Science Tokyo) design system to slides, posters, documents (docx/PDF), figures and web pages — brand colors (Science Blue #1c3177, sub color #7f96c2), Noto Sans JP / Hind / Yu Gothic, logo and university-name rules, arch graphic elements, and the PowerPoint template patterns. Use whenever the user asks for 東京科学大のデザイン, Science Tokyo branding, 科学大のテンプレート, or makes material presented under the university's name.
---

# Science Tokyo デザインガイド

東京科学大学（Science Tokyo）の公式デザインシステム <https://design-system.isct.ac.jp/ja> を、
スライド・文書・図・Web を作るときにそのまま使える形にまとめた非公式の要約。
迷ったら公式ページを優先する（各 reference の末尾に出典 URL がある）。

## 最初に守ること

1. **色はブランドカラーとサブカラーが主役。** Science Blue `#1c3177` とサブカラー `#7f96c2`
   を優先し、拡張色（extended）は強調や区別が必要なときだけ足す。全色を使う必要はない。
   色の比率は、スライドや冊子なら全ページを通して判断する。
2. **書体。** 和文 Noto Sans JP、欧文 Hind。和文の中に混じる欧文は Noto Sans JP のまま。
   PowerPoint / Word などのオフィス文書は游ゴシック（Medium 以上）。
3. **ロゴは作らない。** ロゴを文字やSVGで再現しない。ロゴデータは学内限定サイトの
   ブランドデータダウンロードか公式テンプレートから本人が入れる。Claude/Codex は
   ロゴの位置を空けるか、大学名をテキストで置く（[logo-and-name.md](references/logo-and-name.md)）。
4. **大学名。** 統一名称は「Science Tokyo」。正式名は「東京科学大学」「Institute of Science Tokyo」。
5. **アクセシビリティ。** 公式カラーシステムは WCAG 2.1 AA が基準。本文テキストは
   コントラスト 4.5:1 以上。`#7f96c2` は白地で約 3.0:1 なので**文字色に使わない**（帯・罫線・図形用）。
6. **公式テンプレートのパターン（A〜D）は混ぜない。** 1つの資料では1パターンに統一する。

## 何を作るかで読む reference を選ぶ

| 作るもの | 読む |
|---|---|
| 色を決める・CSS/JSON トークン | [colors.md](references/colors.md)、[assets/tokens.css](assets/tokens.css)、[assets/tokens.json](assets/tokens.json) |
| 書体・文字サイズ | [typography.md](references/typography.md) |
| ロゴ・大学名・組織名の表記 | [logo-and-name.md](references/logo-and-name.md) |
| アーチの帯・背景の図形 | [graphic-elements.md](references/graphic-elements.md) |
| スライド（HTML / PowerPoint / Artifact） | [slides.md](references/slides.md)、[assets/slide-template.html](assets/slide-template.html) |
| docx・PDF・ポスター・グラフ | [documents-and-figures.md](references/documents-and-figures.md)、[assets/science_tokyo.mplstyle](assets/science_tokyo.mplstyle) |

## すぐ使う最小セット

```text
Science Blue   #1c3177   見出し・濃色背景・強調罫線
Sub color      #7f96c2   帯・装飾（文字には使わない）
Navy 700       #435ea5   小見出し・アイブロウ（白地 6:1 以上）
Background 1   #e8eaf1   表ヘッダ・強調ボックス
Background 2   #f2f4f9   カード背景
Navy 200       #cfdbed   罫線・濃色背景上の淡い文字
本文           #333333   白地の本文 / 補足 #595959
```

## 仕上げのチェック

- [ ] 主色が Science Blue とサブカラーで、拡張色は目的のある箇所だけ
- [ ] `#7f96c2` やその他の淡色を文字に使っていない／本文 4.5:1 以上
- [ ] 書体が Noto Sans JP（＋欧文 Hind）、オフィス文書なら游ゴシック Medium 以上
- [ ] ロゴを自作していない（場所を空けた、または利用者に公式データを入れてもらう旨を伝えた）
- [ ] 大学名の表記が「Science Tokyo」「東京科学大学」「Institute of Science Tokyo」のいずれか
- [ ] スライドなら1つのテンプレートパターンに統一、アーチ図形は辺に接して配置
- [ ] 成果物を渡すとき、ロゴ未挿入と公式テンプレートの所在（学内限定）をユーザーに伝える
