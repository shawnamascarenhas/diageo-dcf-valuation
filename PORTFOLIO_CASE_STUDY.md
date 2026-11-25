# Diageo plc discounted cash flow valuation

## Project overview

This project values Diageo plc using a five-year free cash flow to the firm model. It links reported financial history to regional revenue forecasts, normalized operating earnings, reinvestment requirements, WACC, terminal value and a detailed enterprise-to-equity bridge.

The base case produces an implied value of GBP 22.65 per diluted share versus a GBP 15.93 reference price. This represents 42.2% implied upside. The model presents that result as a range because the terminal period contributes approximately 80% of enterprise value.

## Objective

The objective was to build an auditable DCF that demonstrates the complete valuation process:

- Convert company disclosures into structured historical financials.
- Forecast revenue and operating performance under multiple cases.
- Calculate unlevered free cash flow.
- Estimate a market-based discount rate.
- Test the economic consistency of terminal growth.
- Reconcile enterprise value to diluted per-share equity value.
- Expose the principal valuation risks through sensitivity analysis.

## Company selection

Diageo provides a useful DCF case because it combines global operations, regional reporting, strong brand economics and several non-operating valuation judgments. The equity bridge requires specific treatment of net borrowings, pensions, non-controlling interests, associates and joint ventures, disposal proceeds and foreign exchange.

## Model structure

### Historical financials

The historical section organizes reported income-statement, balance-sheet and cash-flow data. Normalization items remain visible so the forecast can distinguish continuing operations from temporary costs.

### Revenue forecast

Revenue is forecast by region under base, upside and downside cases. One master scenario selector routes the chosen assumptions through the operating forecast. The base case assumes a gradual recovery rather than a rapid return to high growth.

### Operating forecast

The operating model forecasts normalized EBIT, taxes, depreciation and amortization, capital expenditure and working capital. Normalized EBIT margin increases from 30.3% in FY2027 to 31.6% in FY2031.

### Free cash flow

FCFF is calculated as normalized EBIT after cash taxes, plus depreciation and amortization, less capital expenditure and the increase in working capital. FY2027 includes restructuring effects. FCFF then normalizes from approximately US$2.7bn in FY2027 to US$4.1bn in FY2028 and reaches approximately US$4.48bn in FY2031.

### Discount rate

The model derives a 7.32% USD WACC using CAPM and a market-value capital structure. The discount-rate currency matches the USD forecast cash flows. Mid-year discounting reflects cash generation throughout each forecast year.

### Terminal value

The primary terminal calculation uses the Gordon-growth method with a 2.50% perpetual growth rate. A 20.0% terminal ROIC implies a 12.5% reinvestment rate, connecting long-run growth to the investment required to support it. The terminal value implies an 11.9x EV to EBITDA multiple, compared with a separate 10.5x exit-multiple cross-check.

### Equity bridge

The DCF produces enterprise value of approximately US$82.8bn. The model then makes the following adjustments:

| Adjustment | US$m | Treatment |
|---|---:|---|
| Enterprise value | 82,837 | Starting value |
| Net borrowings | (20,482) | Deduct |
| After-tax pension surplus | 464 | Add |
| Non-controlling interests | (2,083) | Deduct |
| Associates and joint ventures | 5,284 | Add |
| Expected EABL net sale proceeds | 2,300 | Add |
| Equity value | 68,320 | Result |

Equity value is divided by 2,231m diluted shares and translated into GBP.

## Valuation results

| Metric | Base case |
|---|---:|
| DCF value per share | GBP22.65 |
| Reference share price | GBP15.93 |
| Implied upside | 42.2% |
| Enterprise value | US$82.8bn |
| Equity value | US$68.3bn |
| WACC | 7.32% |
| Terminal growth | 2.50% |
| Terminal ROIC | 20.0% |
| Implied terminal EV to EBITDA | 11.9x |

## Sensitivity analysis

The model tests terminal growth from 1.0% to 4.0% and WACC from 5.5% to 8.5%. The selected lower and higher cases produce GBP20.21 and GBP31.35 per share.

| Terminal growth | 6.5% WACC | 7.3% WACC | 7.5% WACC | 8.0% WACC |
|---:|---:|---:|---:|---:|
| 2.0% | GBP25.71 | GBP21.05 | GBP20.21 | GBP18.14 |
| 2.5% | GBP28.19 | GBP22.65 | GBP21.67 | GBP19.30 |
| 3.0% | GBP31.35 | GBP24.61 | GBP23.45 | GBP20.68 |

The sensitivity confirms that a modest change in long-run assumptions has a material effect on equity value.

## Audit framework

The workbook includes integrated checks for:

- Historical and forecast balance sheets
- Revenue and operating-model links
- Net income and cash-flow consistency
- Cash and debt schedules
- Retained earnings and non-controlling interests
- PP&E and intangible-asset schedules
- WACC and terminal-growth validity
- FCFF period completeness
- Terminal and equity value
- Sensitivity midpoint consistency
- Equity-bridge and share-count arithmetic
- Per-share foreign-exchange translation

The final workbook scan found no standard Excel formula errors, and all implemented checks resolved correctly at export.

## Main limitations

### Terminal-value dependence

Approximately 80% of enterprise value comes from the terminal period. The base valuation therefore depends heavily on WACC, growth and terminal cash economics.

### Book-value proxies

Associates, joint ventures and non-controlling interests use book-value estimates because directly observable market values are unavailable. Economic values may differ.

### Transaction uncertainty

The model adds expected EABL net sale proceeds of US$2.3bn because the operating forecast excludes EABL. Completion timing and final proceeds may differ from the announcement.

### Foreign exchange

The business is valued in USD and translated into GBP per share. Changes in GBP to USD affect the headline valuation.

### Market inputs

The reference price, risk-free rate, beta, equity risk premium, credit spread and capital-structure values require a refresh before any new use of the model.

## What I learned

The project reinforced that a DCF is most useful when the operating assumptions, reinvestment requirements and terminal economics remain connected. A precise price target can conceal substantial uncertainty. The model therefore emphasizes traceable assumptions, cross-checks and valuation ranges rather than relying on a single output.

## Portfolio files

- `Diageo_DCF_Portfolio.xlsx` contains the complete model.
- `Diageo_DCF_Valuation_Memo.pdf` explains the conclusion and methodology.
- `Diageo_DCF_Valuation_Presentation.pptx` provides a seven-slide overview.
- `MODEL_AUDIT_REPORT.md` documents the checks and remaining risks.

This project is an academic portfolio exercise and is not investment advice.
