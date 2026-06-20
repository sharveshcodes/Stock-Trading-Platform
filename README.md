Project Overview: Stock Trading Platform Simulation
What it is: A console-based Java application that simulates a basic stock market environment — users can view live (simulated) prices, buy/sell shares, and track portfolio performance over time, all built with OOP principles.
Purpose
Lets a user practice trading concepts in a risk-free, simulated market — tracking cash, holdings, and profit/loss without real money, while demonstrating clean OOP architecture in Java.
Core Components (Classes)
ClassRoleStockA tradable asset — symbol, company name, price; fluctuate() randomly moves price ±4%MarketHolds all stocks, displays prices, advances all prices on a "tick"TransactionImmutable record of one buy/sell (type, symbol, qty, price, timestamp); converts to/from CSVPortfolioCash balance, holdings map, transaction history; handles buy()/sell() logic and net worth/P&L calculationUserWraps a username with their Portfolio
Features

View Market Data — lists all stocks with current prices
Buy Stock — validates the symbol exists and cash is sufficient before purchasing
Sell Stock — validates the user actually owns enough shares
Portfolio Summary — shows cash, holdings, holdings value, net worth, and overall profit/loss (% and $)
Transaction History — full log of every buy/sell with timestamps
Simulate Market Tick — manually advances prices randomly so the user can see how their portfolio value reacts
Save & Exit — writes cash, holdings, and transaction history to text files for persistence

Persistence (File I/O)

portfolio_data.txt — cash balance + current holdings
transactions_data.txt — full transaction log (CSV format)
Both are auto-reloaded the next time the program runs, so a user's portfolio carries over between sessions

What the Uploaded Demo Shows

User "Sharvesh" starts with $10,000.00 cash
Viewed market data (6 stocks: AAPL, GOOGL, AMZN, MSFT, TSLA, NFLX)
Tried to buy using "3" as a symbol → correctly rejected as "Symbol not found in market" (since "3" isn't a valid ticker — this was likely meant to be a menu choice typed in the wrong field)
Portfolio summary correctly showed no holdings, $10,000 net worth, $0 P/L
Ran a market tick to simulate price movement
Saved and exited cleanly

This run shows the validation logic working correctly — it caught the invalid symbol entry rather than crashing or silently failing.
Tech Stack

Language: Java (standard library only — no external dependencies)
I/O: Plain text/CSV files for persistence
Interface: Console menu-driven

Current Limitations

Single-user only (no multi-account support in the same run)
Flat-file storage rather than a real database
No real-world market data — prices are randomly simulated, not live
Demo link is in my Linkedin Profile
link:https://www.linkedin.com/posts/sharvesh-g-2a5514404_codalpha-internship-java-ugcPost-7473925435622313984-2wTY/?utm_source=share&utm_medium=member_desktop&rcm=ACoAAGdNqZ0BWt9OlPqTzfHGluLKn8E6lOGNSMI
