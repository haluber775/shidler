# [Spec Title]

**Created by:**  
**Updated by:**  
**Date Created:**  
**Date Updated:**  
**Version:**  

---

## 1. Objective  
The objective of this model is to evaluate and compare foreign exchange hedging strategies for a known foreign-currency receivable. The model quantifies USD outcomes under alternative approaches including a forward hedge, a money market hedge, and option-based hedges.

The model is designed to support treasury decision-making by clearly measuring how each strategy reduces downside risk and how it affects upside potential. The analysis focuses on producing consistent, comparable results that allow a decision maker to select a hedge based on risk tolerance, cost, and expected outcomes.

## 2. Scope  
In-scope:
Analysis of a single foreign-currency receivable (FC_AMT)
One-period hedging horizon ending at settlement (T_DAYS)
Forward hedge using the forward rate (F0_in)
Money market hedge using borrowing and lending rates (R_FC, R_USD)
Option-based hedges including:
Protective put
Collar strategy
Deterministic inputs for interest rates, strike prices, and premiums
Scenario-based analysis using a range of future spot rates (S_T)
Calculation of USD proceeds under each strategy
Sensitivity analysis over a defined exchange rate range of plus or minus 5 percent
Comparison of hedge performance across strategies
Out-of-scope:
Multi-period or dynamic hedging strategies
Stochastic modeling or simulation techniques such as Monte Carlo
Explicit option pricing models such as Black-Scholes
Credit risk or counterparty default risk
Transaction costs, bid-ask spreads, or liquidity constraints
Hedge accounting treatment under IFRS or GAAP
Real-time or live market data integration
Portfolio-level hedging involving multiple exposures
## 3. Inputs  
The model requires a complete and explicitly defined set of inputs. These inputs are organized into core transaction data, market data, option parameters, and scenario variables.

Core Data Inputs (Transaction-Specific)
Named Range	Description	Unit
FC_AMT	Foreign-currency receivable amount	FC
T_DAYS	Time to settlement	Days
Market Data Inputs
Named Range	Description	Unit
S0_in	Spot exchange rate at inception	USD per FC
F0_in	Forward exchange rate	USD per FC
R_USD	USD interest rate	Annual %
R_FC	Foreign interest rate	Annual %
Option Parameters
Named Range	Description	Unit
K_PUT	Put option strike	USD per FC
K_CALL	Call option strike	USD per FC
PREM_PUT	Put premium per unit	USD
PREM_CALL	Call premium per unit	USD
Scenario Variable
Named Range	Description	Unit
S_T	Future spot rate at maturity	USD per FC

S_T is varied across scenarios to evaluate sensitivity.

5. Parameters
Parameter	Description	Value
Day-count basis	Interest convention	ACT/360
Time fraction	Year conversion	T_DAYS / 360
Scenario range	Exchange rate variation	±5% around S0_in
Step size	Sensitivity increment	1%

## 4. Workflow / Steps  
1Define Inputs
Enter all required variables including FC_AMT, S0_in, F0_in, R_USD, R_FC, K_PUT, K_CALL, PREM_PUT, PREM_CALL, and T_DAYS.
Establish Unhedged Exposure
Express the USD value of the receivable as a function of the future spot rate (S_T).
Compute Forward Hedge Outcome
Apply the forward rate to determine fixed USD proceeds at settlement.
Construct Money Market Hedge
Calculate the present value of the foreign-currency receivable using R_FC.
Convert the borrowed amount at the spot rate S0_in.
Invest the USD proceeds at R_USD until maturity.
Confirm that the resulting USD value is consistent with forward pricing assumptions.
Evaluate Option Strategies
For the protective put, calculate the payoff under different S_T values and subtract total premium cost.
For the collar, apply payoff conditions based on the put strike (K_PUT) and call strike (K_CALL) and incorporate net premium.
Run Sensitivity Analysis
Vary S_T across a range of plus or minus 5 percent around S0_in using consistent step increments.
Compute USD proceeds for each strategy at every scenario.
Generate Outputs
Compile results into structured tables and charts for comparison.
Interpret Results
Assess trade-offs across strategies in terms of downside protection, upside participation, and cost.
## 5. Expected Outputs  
The model should produce clear, structured outputs that allow direct comparison across hedging strategies and support decision-making.

Primary Deliverables:

Strategy Comparison Table
A table summarizing USD proceeds for each hedging strategy under the base-case scenario.
Sensitivity Table
A structured table showing USD proceeds for each strategy across a range of future spot rates (S_T). The range should reflect ±5% variation around S0_in with consistent increments.
Payoff Chart
A visual representation of USD proceeds as a function of S_T, with separate lines for each strategy. This chart should clearly illustrate:
Downside protection
Upside participation
Breakpoints for option strategies
Key Metrics Summary
A concise set of metrics including:
Minimum USD outcome (worst case)
Maximum USD outcome (best case)
Break-even levels for option strategies
Supporting Calculations
Transparent intermediate calculations for each hedge type to ensure auditability and traceability.
Interpretation Notes
Brief written observations that explain the trade-offs between strategies and highlight the most relevant findings.

## 6. Evaluation Criteria  
The model and specification will be evaluated based on the following criteria:

Accuracy and Analytical Logic

Calculations correctly implement each hedging strategy
Financial relationships, including interest rate parity, are applied consistently
Results are internally coherent across methods

Clarity and Professionalism

Inputs, assumptions, and outputs are clearly defined
Logical flow of calculations is easy to follow
Terminology and structure are appropriate for a treasury or finance audience

Completeness

All required inputs are included with names, values, and units
All hedge strategies are fully implemented
Outputs include both numerical tables and visual analysis

Reproducibility

Another analyst or an AI system can rebuild the model from the specification alone
No ambiguity in formulas, steps, or assumptions

Insight and Decision Usefulness

Outputs clearly communicate trade-offs between strategies
Sensitivity analysis highlights risk and return differences
The model supports a well-informed hedging decision

## 7. AI Prompts (Examples)  
Create a 2–3 page quantitative technical specification for a foreign exchange hedging model using the Excel file FIN312_Haluber_Stage2.xlsx as the base model. Follow the structure and formatting requirements outlined in the Stage 3 specification template. Clearly define the problem statement, inputs with named ranges, assumptions, calculation flow, outputs, and sensitivity analysis. Ensure the document is written at a professional level and is detailed enough for another analyst or AI system to fully reconstruct and improve the model. 
Create a FIN 312 Stage 3 technical specification using the Excel model FIN312_Haluber_Stage2.xlsx. Follow the assignment structure and formatting requirements for the FX hedging project. Use the model inputs, assumptions, and calculations from Stage 2, and produce a clear, professional, and quantitative document that includes problem definition, inputs with units, assumptions, calculation flow, outputs, model review, and sensitivity analysis. Ensure the specification is precise and reproducible so that it can be used directly to generate an improved model in Stage 4.

---
