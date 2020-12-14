# Monte Carlo Value At Risk Introduction

Value at Risk (VaR) is the regulatory measurement for assessing market risk. It reports the maximum likely loss on a portfolio for a given probability defined as x% confidence level over N days. VaR is vital in market risk management and control. Also regulatory and economic capital computation is based on VaR results. Although VaR measure is objective and intuitive, it doesn’t capture tail risk. There are three commonly used methodologies to calculate VaR – parametric, historical simulation and Monte Carlo simulation. This presentation focuses on Monte Carlo VaR.  

Keywords:
Value at Risk, VaR, Monte Carlo VaR, market risk, financial market, trading risk, risk analytics, risk implementation

	Monte Carlo VaR
	Definition
Value at Risk (VaR) is the regulatory measurement for assessing market risk. It reports the maximum likely loss on a portfolio for a given probability defined as x% confidence level over N days. VaR is vital in market risk management and control. 
 

	VaR Roles
	Risk measurement
	Risk management
	Risk control
	Financial reporting
	Regulatory and economic capital

	VaR Pros & Cons
	Regulatory measurement for market risk
	Objective assessment
	Intuition and clear interpretation
	Consistent, flexible and stable measurement
	Doesn’t measure risk beyond the confidence level: tail risk
	Non sub-additive

	VaR Approaches
	Parametric VaR
	Historical VaR
	Monte Carlo VaR

	Monte Carlo Simulation
	Assumption
Assuming market factors follow certain stochastic processes.
	Pros
Easy back and stress test
Good for high confidence level and tail risk
	Cons
Dependent on distribution assumption
Calibration required
Extensive computation

	Monte Carlo VaR Methodology
	Assume each market factor follows certain stochastic process:  ϑ(σ_i W_i) where W is a Wiener process
	Calibrate each volatility σ_i and pair-wise correlation ρ_ij for any two market factors
	Simulate market factor changes δ_i based on the stochastic processes and correlated random variables.
	Generate market scenarios x_i=x_0 δ_i
	Compute scenario PVs:  P(x_i)
	Compute scenario P&L:	P(x_i )-P(x_0)
	Sort all scenario P&Ls. The VaR is the number at 1% lowest level

	VaR Scaling
	Normally firms compute 1-day 99% VaR
	Regulators require 10-day 99% VaR
	Under IID assumption, 10-day VaR = √10*〖VaR〗_(1-day)

	VaR Backtest
	The only way to verify a VaR system is backtest
	At a certain day, compute hypothetic P&L (valuation date and portfolio unchanged)
If (hypothetic P&L > VaR)  breach
	For one year
If number of breaches is 0-4, the VaR system is in Green zone
If number of breaches is 5-9, the VaR system is in Yellow zone
If number of breaches is 10 or more, the VaR system is in Red zone


You can find more details at
https://finpricing.com/lib/IrSwap.html

 
