# 逃げ切り計算機 / Retirement Survival (Runway) Simulator

**バージョン / Version:** v1.2 
**ライセンス / License:** MIT

---

## ⚠️ 免責事項 / Disclaimer

本ツールはあくまでシミュレーション目的のみを対象としており、結果の正確性・完全性を保証するものではありません。投資・財務に関する意思決定は必ずご自身の判断と責任のもとで行ってください。本ツールの利用によって生じたいかなる損害についても、作者は責任を負いません。

This tool is provided for simulation purposes only. No warranty is made regarding the accuracy or completeness of results. All financial and investment decisions should be made at your own discretion and risk. The author assumes no liability for any damages arising from the use of this tool.

---

## 概要 / Overview

**日本語**

「逃げ切り計算機」は、引退後の資産が100歳まで枯渇しないかをシミュレーションするツールです。配当収入を主な収入源とし、元本には一切手をつけないという保守的な設計思想に基づいています。インフレ率の異なる3つのシナリオで同時比較でき、年間収支と現金残高の推移をグラフ・テーブルで可視化します。

**English**

The "Retirement Survival Calculator" simulates whether your post-retirement assets will last until age 100. It is built on a conservative philosophy: dividend income covers all living expenses, and the principal (stock assets) is never touched. Three inflation scenarios run simultaneously, with cash flow and balance projections visualized in both chart and table form.

---

## ⬇️ ダウンロード / Download

**[▶ 最新版をダウンロード / Download Latest Version](https://github.com/toyoji-blip/runway-simulator/releases/latest/download/retirement_calculator.html)**

ダウンロードしたHTMLファイルをブラウザで開くだけで使えます。インストール不要です。  
Download the HTML file and open it in any browser. No installation required.

---

## 特徴 / Features

**日本語**

- 📊 3つのインフレシナリオ（ベース・ワース・ワースト）を同時表示
- 💰 配当収入ベースのシミュレーション（税引き前/後の切り替え対応）
- 📥 収入項目を任意追加（年金・iDeCo・退職金・遺産相続など）
- 💸 ライフイベント出費を任意追加（自宅改装・老健入居金など）
- 📤 設定のJSON export/import（複数シナリオの保存・切り替え）
- 🖥️ ローカル動作・インストール不要・ブラウザで即起動

**English**

- 📊 Three simultaneous inflation scenarios (Base / Worse / Worst)
- 💰 Dividend-based simulation with pre/post-tax toggle
- 📥 Add custom income items (pension, iDeCo, inheritance, severance pay, etc.)
- 💸 Add life event expenses (home renovation, care facility deposit, etc.)
- 📤 JSON export/import for saving and restoring configurations
- 🖥️ Runs locally in any browser — no installation required

---

## 使い方 / How to Use

**日本語**

1. `retirement_calculator.html` をダウンロードし、任意のブラウザで開く
2. 基本設定・収入項目・ライフイベント出費を入力する
3. 「▶ シミュレーション実行」を押す
4. 設定を保存したい場合は「📤 エクスポート」でJSONファイルとして保存する
5. 次回利用時は「📥 インポート」で設定を復元し、シミュレーションを再実行する

> **注意：** 設定内容はブラウザのメモリに保持されません。毎回エクスポートして保存し、次回はインポートして復元してください。

**English**

1. Download `retirement_calculator.html` and open it in any browser
2. Enter your basic settings, income items, and life event expenses
3. Click "▶ シミュレーション実行" (Run Simulation)
4. To save your configuration, click "📤 エクスポート" (Export) to download a JSON file
5. On your next session, click "📥 インポート" (Import) to restore your settings and re-run

> **Note:** Settings are not persisted in the browser. Always export your configuration and import it in the next session.

---

## 入力項目の説明 / Input Guide

**日本語**

### 基本設定
| 項目 | 説明 |
|------|------|
| 引退年齢 | シミュレーション開始年齢 |
| 引退時の現金残高 | 引退時点で手元にある現金（万円） |
| 引退時の配当（年額） | 税引き後の年間配当収入（万円）。税引き前入力も可能（税率設定で自動換算） |
| 年平均増配率 | 毎年の配当成長率（%） |
| 引退初年度の生活費 | 基準となる年間生活費（万円）。翌年以降はインフレ率で増加 |
| 初年度追加費用 | 引退初年度のみ加算される臨時費用（住民税の増加・健康保険料など） |
| インフレ率シナリオ | ベース・ワース・ワーストの3シナリオのインフレ率（%） |

### 収入項目（オプション）
配当以外の収入を追加できます。**必ず税引き後の手取り額を入力してください。** 税額が不明な場合はベストエフォートで構いません。楽観的に見積もるより、20%程度の税率を引いて悲観的に推定する方が安全です。デフォルトでは公的年金（国民年金・厚生年金）のみ設定されています。その他の収入（iDeCo・退職金・遺産相続など）はご自身で追加してください。

- 単年の臨時収入は「単年」チェックをONにしてください
- 同じ収入源でも受取額が年齢によって変わる場合は、期間ごとに別々の項目として登録してください

### ライフイベント出費（オプション）
生活費とは別の一時的・計画的な出費を追加できます。**入力金額はインフレ連動なしの固定額です。** 住宅リフォーム・老健施設入居金・子供の進学費用などを登録してください。

- 単年の出費は「単年」チェックをONにしてください
- 複数年にわたり年額が異なる場合は、期間ごとに別々のイベントとして登録してください

**English**

### Basic Settings
| Field | Description |
|-------|-------------|
| Retirement Age | Age at which simulation begins |
| Cash at Retirement | Cash on hand at retirement (in 万円 / 10,000 JPY) |
| Annual Dividend | After-tax annual dividend income. Pre-tax input available with automatic conversion |
| Annual Dividend Growth Rate | Expected yearly dividend growth rate (%) |
| Annual Living Expenses | Base living cost for year one (万円). Increases with inflation from year two |
| First-Year Extra Costs | One-time additional expenses in the first year (e.g. spike in resident tax, health insurance) |
| Inflation Scenarios | Inflation rates (%) for Base, Worse, and Worst scenarios |

### Income Items (Optional)
Add income sources other than dividends. **Always enter after-tax amounts.** If the exact tax is unclear, a best-effort estimate is fine — erring on the pessimistic side (e.g. deducting ~20%) is safer than being optimistic. Only public pension (国民年金 / 厚生年金) is pre-configured. Add other income sources (iDeCo, severance pay, inheritance, etc.) as needed.

- For one-time income, check the "単年" (single year) checkbox
- If the same income source pays different amounts at different ages, register each period as a separate item

### Life Event Expenses (Optional)
Add planned lump-sum or recurring expenses separate from living costs. **Amounts are fixed and do not increase with inflation.** Examples: home renovation, care facility deposit, children's tuition.

- For single-year expenses, check the "単年" (single year) checkbox
- If amounts differ across years, register each period as a separate item

---

## 設計思想 / Design Philosophy

**日本語**

本ツールは意図的に**悲観的**な設計になっています。

- 収入は配当金のみをベースとし、株式資産（元本）の取り崩しは一切考慮しません
- 生活費はインフレで増加し続けますが、配当は控えめな増配率で成長します
- 税金は生活費に含まれない想定のため、収入はすべて税引き後で入力します
- 株式資産の取り崩しによるシミュレーションには対応していません

「現金残高 > 0」を100歳まで維持できれば逃げ切り成功です。

**English**

This tool is intentionally **pessimistic** by design.

- Only dividend income is counted as revenue; the stock principal is never drawn down
- Living expenses grow continuously with inflation, while dividends grow at a conservative rate
- Tax on living expenses is not modeled separately — all income inputs are expected to be after-tax
- Simulation of asset liquidation (selling stocks) is not supported

If cash balance remains above zero through age 100, you've made it.

---

## 動作環境 / Environment

**日本語**

- インストール不要。HTMLファイルをダウンロードしてブラウザで開くだけです
- Chrome / Firefox / Safari / Edge など主要ブラウザで動作します
- インターネット接続不要（ローカル動作）
- スマートフォンでも動作しますが、PC・タブレットでの利用を強く推奨します

**English**

- No installation required. Simply download the HTML file and open it in any browser
- Compatible with all major browsers: Chrome, Firefox, Safari, Edge
- Works fully offline
- Mobile-compatible, but desktop or tablet is strongly recommended for the best experience

---

## ライセンス / License

CC BY-NC-ND 4.0 — 非商用・改変禁止・クレジット表示必須  
Commercial use and derivative works are prohibited without permission.  
https://creativecommons.org/licenses/by-nc-nd/4.0/
