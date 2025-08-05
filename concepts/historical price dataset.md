Most price feeds provide, per time point: 

| Column Name          | Meaning                             |
| -------------------- | ----------------------------------- |
| `Date` or `Datetime` | Timestamp for the price             |
| `Open`               | Price at start of time interval     |
| `High`               | Highest price during that interval  |
| `Low`                | Lowest price during that interval   |
| `Close`              | Price at the end of the interval    |
| `Adj Close`          | Close adjusted for dividends/splits |
| `Volume`             | Number of shares traded             |
|                      |                                     |
We compute the log returns between adjacent closing prices over days [[log return]] 
We compute the [[volatility]] 
