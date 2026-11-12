# KHO Bot public research

[Open the published report](https://maidh91.github.io/kho-bot-public/) or open [index.html](index.html) directly from disk. The file is self-contained; no server or downloads are needed. Changes on a PR branch are local previews until merged and deployed.

The November 2026 campaign shows three preset objectives and five representative choices per preset. Overview cards, findings, adverse cost comparisons and sortable results are preserved. Each choice opens:

- Rounded monthly equity, month-end drawdown, adjustable rolling returns, date filters and yearly/monthly returns.
- All recorded simulated trade exits, including partial closes, with entry/exit prices, size, direction and profit. Click a row for times, holding period, original stop/target, costs, run funding and ambiguity flags.
- Setup statistics: win rate, average win/loss, profit factor, median holding time and exit charges. New charts show cumulative exit profit, outcome distribution and holding time versus profit.
- Recorded strategy-selection timelines and vault runs, funding fractions, run returns, stopouts and weekly pause reasons where available.

The 15 choices contain 65,476 exits. The HTML is about 4.29 MB. Setup and position names are anonymous. The historical search used all shown periods; these are simulations, not forward tests or live account records. Month-end drawdown can understate the saved full-path maximum. Exit profit and explicit exit charges are not total account profit or all trading costs. Unknown fields remain unknown; no within-minute path or unrealized excursion is invented.

Exact configuration files, strategy rules, source/input identities, raw journals, broker data and market history remain private. Full simulated trade projections are intentionally public, following the owner's request. This replaces the earlier aggregate-only policy; it does not authorize copying private archives wholesale.

The exporter and regression tests live in the private research repository, alongside the shared report renderer. Run `npm run report:public -- --archive studies/<study>/index.html --template /path/to/kho-bot-public/index.html --output /path/to/new-public.html` there. It validates the reviewed public selections and rounded summary against the source, then builds an explicit allowed-field projection. It refuses to overwrite output and never commits, pushes or deploys. Review the new HTML, including its compressed payload, before replacing this page. Adding a new campaign or changing the fifteen selections needs a reviewed overview/summary template first.

Verification: all 65,476 recorded exit values reconcile with the private source. Offline Chrome checks cover filtering, numeric sorting, charts, adjustable rolling windows, trade pagination and the row-detail modal. No new strategy search or backtest is part of this presentation update.
