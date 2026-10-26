# market-charts

兩份以官方／公開資料建置的互動分析頁，皆為單檔離線 HTML（無 CDN、無追蹤、無外部請求）。

| 頁面 | 內容 | 主要資料來源 |
|---|---|---|
| [`ust-curve-2026.html`](ust-curve-2026.html) | 美國公債殖利率走勢（2026 YTD，14 個期限），可切換期限／利差／區間變動，標註 FOMC、CPI、非農、10 年期標售 | U.S. Treasury Daily Par Yield Curve、Federal Reserve FOMC 日程、BLS 公布日程、TreasuryDirect |
| [`ls-vs-dca-lab.html`](ls-vs-dca-lab.html) | 一次投入（LS）vs 定期定額（DCA）的起點敏感度實驗室：9 個標的、逐月起點、IRR 年化、滾動起點勝率 | Yahoo Finance 月線收盤 |

入口頁：`index.html`（GitHub Pages 首頁）。

## 口徑

- 殖利率頁為官方收盤值（每日）；盤中即時報價可能與收盤差數 bp。
- 報酬頁一律為**價格報酬**：不含股息、不含稅費與匯率，總投入固定 100,000。
- 年化：LS 用 `(期末 ÷ 投入)^(12/月數) − 1`；DCA 用每月現金流解 IRR 後以 `(1+r)¹² − 1` 年化。

僅供研究與教學，不構成投資建議。
