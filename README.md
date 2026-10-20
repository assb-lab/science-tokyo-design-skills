# science-tokyo-design-skills

東京科学大学（Science Tokyo）のデザインシステムに沿って、Claude Code や Codex が
スライド・文書・図・Web を作るためのエージェントスキル。

- 公式: <https://design-system.isct.ac.jp/ja>
- このリポジトリは研究室内向けの**非公式の要約**。デザインシステムの著作権は東京科学大学に
  帰属する。外部に公開・再配布しない。
- ロゴデータは含めていない。ロゴと公式 PowerPoint テンプレートは、学内限定の
  デザインシステム（完全版）のブランドデータダウンロードから各自で入手する。

## インストール

[skills CLI](https://github.com/vercel-labs/skills) を使う。private リポジトリなので、
GitHub にログイン済み（`gh auth login` か SSH 鍵）であること。

Claude Code と Codex の両方に入れる（ユーザー全体）:

```bash
npx skills add assb-lab/science-tokyo-design-skills -g -a claude-code -a codex
```

プロジェクトだけに入れる場合は `-g` を外す。中身だけ確認したいとき:

```bash
npx skills add assb-lab/science-tokyo-design-skills --list
```

更新:

```bash
npx skills update
```

## 中身

```
skills/science-tokyo-design/
├── SKILL.md                      # 最初に読む要点とチェックリスト
├── references/
│   ├── colors.md                 # ブランド・拡張色・navy系列・コントラスト・グラフ配色
│   ├── typography.md             # Noto Sans JP / Hind / 游ゴシック、サイズの目安
│   ├── logo-and-name.md          # ロゴの扱い（再現しない）、大学名・組織名
│   ├── graphic-elements.md       # アーチの帯の置き方、SVG 例
│   ├── slides.md                 # 公式テンプレートの構成、HTML / pptx の型
│   └── documents-and-figures.md  # docx、ポスター、matplotlib、CSS
└── assets/
    ├── tokens.css / tokens.json  # 色・書体のトークン
    ├── science_tokyo.mplstyle    # matplotlib スタイル
    └── slide-template.html       # 16:9 スライド雛形（ダミー内容）
```

## 使い方の例

- 「この発表を東京科学大のデザインでスライドにして」
- 「科学大の配色で matplotlib の図を描き直して」
- 「Science Tokyo のスタイルで A4 の報告書（docx）を作って」

## 更新するとき

公式サイトの内容が変わったら `references/` を直し、出典 URL を残す。公式の文章を
長くそのまま写さず、要点と数値（色・サイズ）をまとめる形にする。
