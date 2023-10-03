Also known as 'landau notation'
- Captures the core behaviour of a function and hides irrelevant details
- Used to describe **runtime cost**
- Informally, think of O(f(n)) meaning “of the order of f(n)”
### Formal Definition
f(n) is O(g(n)) if there exist constants c > 0 and m >= 0 such that for all n >= m we have f(n) <= c · g(n) 
- For n big enough, f(n) grows no faster than a scaled g(n)