# broker-export-formats

A collection of anonymized options activity files from retail brokers. The kind of CSV or spreadsheet your broker lets you download.

We want options history, plus the stock rows that come with it (assignment, exercise, the wheel). Every broker writes those events a little differently. These samples exist so people building importers can see the real layout instead of guessing from docs.

## What to send

A short excerpt is better than your whole history. Keep the header row, and keep related rows together (the assigned put and the shares that showed up).

Especially useful:

- Multi-leg spreads and rolls
- Expirations, assignments, exercises, and share deliveries
- Cash-settled index options (SPX, XSP, NDX, SPXW)
- Splits and contract adjustments
- Transfers-in (including shares with no cost basis)
- Short stock and buy-to-covers

If your broker has no download at all, open an issue and say so.

## How to contribute

You do not need to know Git. Open an [issue](https://github.com/wrench7/broker-export-formats/issues/new), attach the file, and mention the broker. If you prefer a pull request, put it under `samples/<broker>/`.

Please remove your name, account number, SSN/SIN, address, and bank details. Tickers, dates, and quantities can stay. Scaling the dollar amounts is fine as long as the relationships stay real (100 shares per contract, strike is the delivery price).

By opening an issue or pull request you agree to release the file under CC0 (Creative Commons Zero v1.0 Universal).
