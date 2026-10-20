# 文書・ポスター・グラフ

## Word / docx（docx-js、python-docx）

| 要素 | 設定 |
|---|---|
| 本文 | 游ゴシック Medium 10.5–11 pt、`#333333`、行間 1.5 前後 |
| 見出し1 | 游ゴシック Bold 14–16 pt、`#1c3177` |
| 見出し2 | 游ゴシック Bold 12–13 pt、`#435ea5` |
| 表 | ヘッダ行の塗り `#e8eaf1`（docx-js は `ShadingType.CLEAR`）、罫線 `#cfdbed` |
| 強調枠 | 塗り `#f2f4f9`、左罫線 `#1c3177` |
| ヘッダー | 右上にロゴの空き（公式のレターヘッドがあればそれを使う） |

英語の論文原稿など学外の投稿規定がある文書は、そちらの規定を優先する（色やロゴは入れない）。

## ポスター（A0 など）

- 上部に Science Blue の帯（タイトル帯）、下端か角にサブカラーのアーチの帯。帯は辺に接して置く。
- タイトルは白文字（Science Blue の帯の上）、本文は白地に `#333333`。
- ロゴは帯の外の白地に置く（公式データを利用者が配置）。

## グラフ（matplotlib）

[assets/science_tokyo.mplstyle](../assets/science_tokyo.mplstyle) を使う:

```python
import matplotlib.pyplot as plt
plt.style.use("path/to/science_tokyo.mplstyle")
```

- 系列色の順は `#435ea5` → `#fb5b01` → `#00a3bf`（色覚多様性チェック済み）。4系列以上は
  線種・マーカーを併用するか、図を分ける。
- 段階的な量（時間・温度・濃度の段階など）は navy の濃→淡 `#0a1541 #1c3177 #435ea5 #5f7ab6 #7f96c2`。
- 背景は白、グリッド `#e8eaf1`、軸と目盛り `#595959`。
- 書体は matplotlib に Noto Sans JP / Hind が入っていればそれを使い、無ければ既定のまま
  （図中の文字は英語にしておくと崩れにくい）。

## Web（CSS）

[assets/tokens.css](../assets/tokens.css) をそのまま読み込めば、`--st-*` の変数で
ブランドカラー・navy 系列・拡張色・書体が使える。公式の Web コンポーネント
（Science Tokyo UI、MIT ライセンス）を使える場合はそちらを優先する。
