What are certain advantages of using pandas-based vectorised operation rather than a for loop or recursive function? 
1. Faster processing: because pandas use vectorised operations under the hood, which are implmented in C and means it's much faster than Python loops 
2. Easier readability: one line conveys the whole intent - cleaner code is easier to maintain and debug 
3. More reliable: fewer moving parts, no indexing bugs or off-by-one errors 