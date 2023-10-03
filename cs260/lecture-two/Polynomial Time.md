An algorithm is said to be **poly-time** if it the [[Desirable Algorithm Scaling Property|desirable scaling property]] holds
## Efficiency
Informally, we can consider an algorithm to be **efficient** if it's runtime is polynomial. 
### Justification
It *mostly* works for real-world problems.
- Some poly-time algorithms have high constants and/or exponents (e.g. although N^20 is technically poly-time, it would be useless in practice), so are impractical
	- Instead, they prove something about the problem