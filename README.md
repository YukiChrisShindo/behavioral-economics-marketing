# behavioral-economics-marketing

行動経済学の視点から、製品・サービスの改善案を提案するClaude用のスキルです。

LPのURL、画面のスクリーンショット、製品の説明文などを渡すと、顧客ジャーニーに沿って「どこで・なぜユーザーの行動が止まっているか」を見立て、検証方法つきの改善案をまとめた提案書を作ります。

## できること

- 「コンバージョンを上げたい」「解約を減らしたい」「価格の見せ方を考えたい」といった相談に、行動経済学の効果（アンカリング、デフォルト効果、ピーク・エンドの法則など）をもとに答える
- 仮説ごとに「観察 → メカニズム → 介入案 → 検証方法 → 副作用」をセットで出す
- 最優先の打ち手を1つに絞り、インパクトと実装コストで優先順位をつける
- トラフィックが少なくA/Bテストが成立しない場合は、先行指標や定性調査など現実的な検証方法を提案する
- ダークパターン（偽の希少性、解約の妨害、偽レビューなど）は提案せず、「やらないほうがいいこと」として理由つきで明示する
- 提案書はHTMLのページとして出力する

各効果には、最近の追試・メタ分析をふまえた「当てになる度」（◎○△）がついています。教科書ほど強くないと分かっている効果（損失回避、選択過多、希少性）は、提案の柱にしないようになっています。

## 使い方

相談するだけでスキルが使われます。例：

- 「このLPの申込率を上げたい」＋URL
- 「無料トライアルからの有料転換が8%で止まっている。どこを直せばいい？」
- 「アプリの課金導線を、ユーザーに嫌われずに見直したい」

## インストール

### Claude（claude.ai／デスクトップアプリ）

このリポジトリのフォルダをZIPにして（または配布されている `.skill` ファイルを）チャットに添付し、表示される「Save skill」で保存します。

### Claude Code

スキル用のフォルダにcloneします。

```bash
# 自分の全プロジェクトで使う場合
git clone https://github.com/YukiChrisShindo/behavioral-economics-marketing ~/.claude/skills/behavioral-economics-marketing

# 特定のプロジェクトだけで使う場合
git clone https://github.com/YukiChrisShindo/behavioral-economics-marketing .claude/skills/behavioral-economics-marketing
```

## ファイル構成

```
SKILL.md                         スキル本体（進め方、出力フォーマット、倫理のライン）
references/bias-catalog.md       認知バイアス・心理効果のカタログ（ジャーニー段階別、当てになる度つき）
references/journey-questions.md  ジャーニー各段階の診断質問集
references/experiment-design.md  検証方法の設計（A/Bテスト、サンプルサイズ目安、定性検証）
evals/evals.json                 動作確認用のテストケース
```
