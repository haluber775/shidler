
# FX Hedging Decision Memo – EUR Receivable Exposure

**Created by:** Christian Haluber
**Updated by:** Christian Haluber
**Date Created:** 2026-04-06
**Date Updated:** 2026-04-06
**Version:** 1.0
**LLM Used:** ChatGPT 4.0

---

## Executive Summary (≤150 words)

Our aerospace division expects to receive EUR 20,000,000 in one year from a European customer. At current market conditions, this exposure is highly sensitive to EUR/USD fluctuations. Using the 1-year forward rate of 1.0935, the receivable is currently valued at approximately $21.87 million, but this value is uncertain.

A depreciation of the euro would directly reduce USD proceeds and compress margins on a fixed-price contract. For example, a 5% decline in EUR/USD could reduce proceeds by over $1 million. This memo outlines the exposure, explains the associated risks, and introduces three hedging strategies—forward contracts, currency options, and a money market hedge.

Subsequent stages will develop a quantitative model, document methodology, and provide a final hedge recommendation.
---

## Background & Objectives

Our firm has contracted to deliver aerospace components to a European buyer, with payment of EUR 20,000,000 due in 12 months. Because our cost base and financial reporting are denominated in USD, any weakening of the euro relative to the dollar reduces realized revenue and profitability.

Given ongoing FX volatility driven by interest rate differentials, macroeconomic uncertainty, and global trade conditions, this exposure is financially material.

Primary objective: Protect the USD value of the EUR 20M receivable from adverse FX movements.
Secondary objective: Retain upside potential if the euro appreciates, where economically justified.

---

## Methods

Three hedging strategies will be evaluated:
| Strategy | Mechanism | Pros | Cons |
|----------|-----------|------|------|
| **Forward Contract** | Lock in sale of EUR 20M at forward rate (1.0935) | Eliminates uncertainty; no upfront cost; simple | No upside participation if EUR strengthens |
| **Currency Options** | Purchase EUR put option (premium $0.019/EUR ≈ $380,000 total) | Downside protection with upside participation | Premium reduces net proceeds |
| **Money Market Hedge** | Borrow EUR, convert to USD at spot, invest at USD rate | Synthetic forward; no derivatives required | Uses balance sheet; depends on interest rates |

Each strategy will be evaluated across a range of EUR/USD outcomes (e.g., 0.95–1.20) to compare USD proceeds, breakeven levels, and risk profiles.
---

## Limitations & Next Steps

**Limitations:** Interest rates (USD and EUR) are currently unspecified and will be incorporated in Stage 2.
Option strike prices are assumed near at-the-money and will be confirmed with market data.
Transaction costs and credit considerations are not yet modeled.

**Next Steps:**

1. **Excel Model Build (Stage 2):** Build a model comparing hedge outcomes across FX scenarios
2. **Technical Specification (Stage 3):** Document model structure and assumptions
3. **Final Analysis & Recommendation (Stage 4):** Select optimal hedge strategy based on quantitative analysis

---

## References

- EURUSD spot and forward rates: to be sourced from Bloomberg/Yahoo Finance at Stage 2 initiation.
- Hull, J.C. *Options, Futures, and Other Derivatives*, 11th ed. Pearson.
- Eun, C.S. & Resnick, B.G. *International Financial Management*, 9th ed. McGraw-Hill.
