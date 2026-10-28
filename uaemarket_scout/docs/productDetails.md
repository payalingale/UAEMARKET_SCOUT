# UAE Market Scout: Requirements v0.1

## 1. Problem

Financial advisors spend about 2 hours every morning researching UAE stocks by hand.

## 2. Users

- Advisor: runs the agent, reads and checks the PDF, decides what to tell clients
- Client: never uses the agent; the advisor picks a profile that matches them.

## 3. What we are building

An agent that researches UAE stocks for the advisor and delivers a daily PDF with:

- up to 10 suggested stocks, each with reasons AND risks
- stocks skipped when data is old, missing or contradictory (verdict: insufficient)
- "don't invest today" when nothing is good enough
  Research uses only trusted sources: APIs, company statements, trusted news. Never finfluencers.

## 4. Scope

In: research + daily PDF of up to 10 stocks
Out:

- Buying stocks on behalf of client
- Sharing the pdf with client
- We wont suggest clients to sell
- No stocks will be suggested outside of uae market

## 5. How we know it works

1. Research time: 2 hours → 20 minutes
2. Advisor agrees with at least 7/10 verdicts
3. Never suggests a stock with old or missing data
4. Every reason in the PDF has a source link
5. Never more than 10 stocks, never too much in one sector

## 6. Assumptions (to confirm with the advisor after the demo)

- He spends about 2 hours a day on research
- He would trust it at 7/10 agreement
- Standard profiles (Cautious / Balanced / Aggressive) are enough, not per-client
- Both ADX and DFM stocks are wanted
- Free data sources are acceptable
- A daily PDF is the format he wants
- Shariah filter: optional setting, off by default

## 7.Working steps

- Advisor picks a profile from [cautious/balanced/aggressive]
- Agent collects information from apis,company statements and daily news
- removes stocks with old or missing data.
- Code calculates risk,price changes,daily trading
- AI gives verdict on each stocks at a time [invest, avoid, or not sure]
- Agent picks upto 10 stocks from list based on (max 2 stocks per sector)
- creates the daily PDF: suggested stocks with reasons, risks and source links, plus skipped stocks with the reason.
- Advisor checks the PDF
