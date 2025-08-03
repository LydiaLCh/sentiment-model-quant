![[Screenshot 2025-08-03 at 12.17.28.png]]
Why is only the close price used? because the closing price of the previous day and the opening price of the next day are not necessarily going to be the same 
The best way to compute it is using Pandas (or NumPy) which allows computing differences between rows using vectorised operations like .shift() or .pct_change()

[[Pandas vs Python]]


