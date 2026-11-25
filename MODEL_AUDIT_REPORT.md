# Diageo DCF model audit report

Audit date: 12 September 2026  
Model: `Diageo_DCF_Portfolio.xlsx`  
Scope: workbook calculations, valuation mechanics, supporting deliverables and submission risks

## Audit conclusion

The workbook passed the implemented formula-error scan and every visible model check. The three-statement model, DCF valuation, sensitivity midpoint and enterprise-to-equity bridge reconcile within their stated tolerances. The presentation also passed structural, layout, font-policy and native-chart packaging validation.

The audit does not establish that the assumptions are correct or that the valuation will remain current. Market-dependent inputs and transaction assumptions require a final refresh before submission. Several bridge items use book-value proxies, and terminal value represents about 80% of enterprise value.

## Headline outputs

| Output | Value | Audit observation |
|---|---:|---|
| DCF value per diluted share | GBP22.65 | Ties to the equity bridge and sensitivity midpoint |
| Reference share price | GBP15.93 | Time-sensitive input that should be refreshed |
| Implied upside | 42.2% | Formula-driven comparison with the reference price |
| Enterprise value | US$82.8bn | Equals the present value of explicit FCFF and terminal value |
| Equity value | US$68.3bn | Reconciles through the non-operating bridge |
| WACC | 7.32% | Exceeds the 2.50% terminal growth rate |
| Diluted shares | 2,231m | Issued shares less own shares plus dilution |
| Terminal value share of EV | About 80% | Main source of valuation sensitivity |

## Workbook checks

### Integrated three-statement checks

| Check | Result | Tolerance |
|---|---:|---:|
| Historical balance sheets | 0.0 | US$0.1m |
| Forecast balance sheets | Less than US$0.1m | US$0.1m |
| Revenue build to operating model | 0.0 | US$0.1m |
| Net income to cash flow | 0.0 | US$0.1m |
| Closing cash to balance sheet | 0.0 | US$0.1m |
| Debt schedule to balance sheet | 0.0 | US$0.1m |
| Retained earnings schedule | 0.0 | US$0.1m |
| NCI schedule | 0.0 | US$0.1m |
| PP&E schedule | 0.0 | US$0.1m |
| Intangibles schedule | 0.0 | US$0.1m |
| Scenario selector validity | 0.0 | US$0.1m |

### DCF checks

All nine DCF checks return `OK`:

- WACC exceeds terminal growth.
- All FCFF forecast periods are populated.
- Terminal value is positive.
- Equity value is positive.
- The sensitivity midpoint equals the base DCF result.
- The DCF valuation ties to the equity bridge.
- The diluted share-count bridge reconciles.
- The per-share translation reconciles.
- Expected EABL proceeds enter the bridge once.

### Equity-bridge checks

All six equity-bridge controls return `OK`. These controls independently test the basic and diluted share counts, equity-value arithmetic, valuation tie, per-share translation and EABL treatment.

### Formula errors

The final workbook scan found no `#REF!`, `#DIV/0!`, `#VALUE!`, `#NAME?`, `#N/A`, `#NUM!`, `#NULL!`, `#SPILL!` or `#CALC!` results.

## Valuation mechanics

### Explicit forecast

The model forecasts five years of FCFF. FY2027 includes restructuring effects, after which FCFF normalizes from approximately US$2.7bn to US$4.1bn in FY2028. FY2031 FCFF reaches approximately US$4.48bn.

### Discounting

The model uses a 7.32% USD WACC and mid-year discounting. The timing convention applies discount periods from 0.5x to 4.5x, which is consistent with cash generation through each forecast year.

### Terminal value

The primary terminal calculation uses Gordon growth at 2.50%. The model checks the result against a 20.0% terminal ROIC, a 12.5% required reinvestment rate and an implied 11.9x terminal EV to EBITDA multiple. A separate 10.5x exit multiple provides an additional reasonableness check.

### Enterprise-to-equity bridge

The bridge deducts US$20.482bn of net borrowings and US$2.083bn of non-controlling interests. It adds a US$464m after-tax pension surplus, US$5.284bn of associates and joint ventures and US$2.3bn of expected EABL net sale proceeds. The resulting US$68.320bn equity value is divided by 2,231m diluted shares and translated into GBP.

## Source review

The workbook contains a dedicated `DCF Sources` worksheet. The final equity bridge cites the FY2026 annual filing and the EABL transaction announcement. Market inputs and other valuation assumptions are recorded in the same source register.

The source record improves auditability, but it does not remove the need to refresh market-dependent information before submission. Any updated input should retain its source URL, date and units.

## Material judgment areas

### Terminal assumptions

Terminal value contributes about 80% of enterprise value. Small changes in WACC or terminal growth therefore produce material changes in per-share value. The selected sensitivity range spans GBP20.21 to GBP31.35.

### Associates and joint ventures

The model adds US$5.284bn at book value because the FCFF forecast excludes associate and joint-venture earnings. Book value may differ from fair value.

### Non-controlling interests

The model deducts US$2.083bn at book value. A market-based value is not directly observable, so the adjustment may not match economic value.

### EABL proceeds

The forecast excludes EABL operations and adds expected net disposal proceeds of US$2.3bn. Completion timing, transaction costs and final proceeds may differ from the announcement.

### Pension tax

The model applies a 25% marginal tax rate to the net pension surplus. This treatment is transparent but simplified.

### Foreign exchange

The DCF remains in USD through equity value and translates the per-share result into GBP. The selected spot rate directly affects the reported GBP value.

## Presentation validation

The seven-slide presentation passed the following automated checks:

- PPTX package integrity
- Slide count and 16:9 geometry
- Heading-fit and layout validation
- Font policy using Helvetica Neue
- First-party PPTX re-import
- Four required native quantitative charts
- Embedded workbook snapshots for all chart data

The final slides were rendered and reviewed visually. One equity-bridge label collision found during the first render was corrected before delivery.

Native PowerPoint execution and native font rendering were not verified because the deck was not opened and edited inside Microsoft PowerPoint. The validation confirms package structure and rendered appearance, not every behavior of the desktop application.

## Submission refresh list

Refresh the following inputs immediately before sending an application:

1. Diageo reference share price
2. GBP to USD exchange rate
3. Risk-free rate
4. Equity risk premium
5. Beta
6. Cost of debt and credit spread
7. Capital-structure market values
8. EABL transaction status and expected proceeds
9. Any new company guidance or reported results

After refreshing the inputs, confirm that the master model status remains `MODEL OK`, the sensitivity midpoint still equals the base valuation and every source entry has a current date.

## Suggested future enhancements

- Add a comparable-companies valuation and football field.
- Replace book-value estimates for associates and NCI with market-based values where reliable data exists.
- Add brand or category drivers beneath the regional revenue forecast.
- Add quarterly forecasts for the first two years if the application benefits from greater operating detail.
- Add a compact change log showing each refreshed market input and its valuation effect.

## Final assessment

The project demonstrates an integrated valuation process from reported financial statements to per-share value. The strongest evidence is the connection between the operating forecast, FCFF, discount rate, terminal economics, sensitivity analysis and equity bridge. The main limitation is the concentration of value in the terminal period, followed by book-value proxies and time-sensitive market inputs.
