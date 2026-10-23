# Bitcoin Trading Bot (Country Manager Edition)

## The Strategy
The core idea is a simple "Mean Reversion / Dip Buying" strategy. 
- **When it buys:** It monitors the last 10 minutes of closing prices. If there is a sudden drop of 0.3% or more, it buys the dip, assuming a quick bounce.
- **When it sells:** It sells as soon as the price rises by 0.4% from the buy price (to secure profit), OR at the very last candle of the 24h window (to satisfy the "flat at the end" rule).

## How I came up with it & What didn't work
As a B2B Sales Leader and Country Manager candidate, my core skill is finding solutions using the best tools available. I am an AI-native professional, so I partnered with AI (Google Gemini / Claude) to architect and write this Python script. 

**What didn't work (The Business Reality Check):**
I quickly realized the "trick" in this assignment. Trying to guarantee a profitable bot that executes at least 5 trades every single random 24h period, while paying a massive 0.2% round-trip fee (0.1% buy + 0.1% sell), is mathematically unfeasible using a rigid set of rules on 1-minute candles. The fees completely eat the margins in ranging or bearish markets. As a Country Manager, my job is to report the truth, not fake the numbers. I built the tool, and the tool proved my business hypothesis: the unit economics of high-frequency trading with 0.2% fees don't scale predictably.

## AI Tools Used
- Prompt engineering and code generation via Google Gemini Advanced / Claude.
- VS Code for execution.

## How to run it
Prerequisites: Python 3.x installed. No external libraries or API keys required.
Command: `python bot.py`
