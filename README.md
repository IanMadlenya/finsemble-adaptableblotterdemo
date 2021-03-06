# Demo of Adaptable Blotter using Finsemble

This demo contains 3 blotter types:
* Trades Blotter
![Trades Blotter](https://raw.githubusercontent.com/jonathannaim/finsemble-adaptableblotterdemo/master/doc/tradeblotter.jpg)
* Positions Blotter
![Positions Blotter](https://raw.githubusercontent.com/jonathannaim/finsemble-adaptableblotterdemo/master/doc/positionblotter.jpg)
* Prices Blotter
![Prices Blotter](https://raw.githubusercontent.com/jonathannaim/finsemble-adaptableblotterdemo/master/doc/priceblotter.jpg)

## Generated data updates
* Trades Blotter : a new trade is added every 5secs
* Positions Blotter : Pnl and Position are recomputed everytime there is a change in the trades or prices data
* Prices Blotter : consensus data is ticking every 1sec

## Edited Data
In all blotter, editable data is bold.
* Trades Blotter : Notional is editable. When edited the "Last Updatded" column is updated and the Position Blotter reflect the new change
* Positions Blotter : No data is editable
* Prices Blotter : Price and BidOffer are editable. When edited the columns Bid, Ask and ChangeOnDay are recomputed and the Position Blotter reflect the new data

## Configuration Data
The blotters are shipped with default configuration data. You can nevertheless configure the blotters differently and every widget will save its own configuration. i.e. you can open 2 Trades Blotter and configure them differently
* Trades Blotter : Sort descending on Trade Id by default so new trades appears at the top
* Positions Blotter : Columns Pnl, CurrentPrice, Position are flashing. And some widget from the dashboard are hidden
* Prices Blotter : Columns BloombergBid, BloombergAsk, Bid, Ask, ChangeOnDay are flashing

## Linked Widgets
For the purpose of the demo, if you link blotters together they will maintain the quick search text value 
See below where the Trades and Positions Blotter are linked
![quicksearch](https://raw.githubusercontent.com/jonathannaim/finsemble-adaptableblotterdemo/master/doc/quicksearch.jpg)

When linking, ChartIQ and Adaptable Blotters together they will link on the "symbol" topic. On the blotter, when you select a cell
in the column Instrument Id, it will show the corresponding symbol information in the widgets such as News and Advanced Chart. On a 
ChartIQ component, when you lookup for a symbol, it will set the Quick Search test of the linked Blotter to that symbol
See below where the Position Blotter, Trade Blotter, News and Advanced Chart are linked
![chartiq](https://raw.githubusercontent.com/jonathannaim/finsemble-adaptableblotterdemo/master/doc/chartiq.jpg)