---
tags:
  - lambda-calculus
  - combinatory-logic
---
- Mathematical background -> Combinatory logic
- Combinatory logic is an alternative to the predicate logic on which Boolean algebra and predicate calculus is based on.
- Combinatory logic provides a bases for lambda calculus and functional programming 
- We can translate between Predicate logic and Combinatory logic 
	- Hence all the Boolean algebra based logic circuits can be translated to equivalent lambda calculus expressions
- combinators are basic building blocks of combinatory logic analogues to Boolean logic gates from predicate calculus  

```scheme
(define I (λ (x) x))
(define K (λ (x y) x))
(define S (λ (x y z)
			(x z (y z))))
			
((S K K) x) => (I x)
(define C (λ (f g x) 
			 ((f x) g)))
			 
(define B (λ (f g x) 
			 (f (g x))))
 
```

#todo understand Y-combinator
