---
tags:
  - "#conventional-interfaces"
---
| Interface | abstraction |
| --------- | ----------- |
| `map`     |             |
| `accum`   |             |
| `filter`  |             |
| `accum-n` |             |
| `mmap`    |             |
# Classic Interfaces 
## map
```scheme 
(define (map proc seqs)
  (if (null? seqs)
      seqs
      (cons (proc (car seqs))
            (map proc (cdr seqs)))))

=> (map proc (x_0 x_1 x_2 ... x_n)) 
=> ((proc x_0) (proc x_1) (proc x_2) ... (proc x_n))
```
## reduce \ accumulate
### Right fold
```scheme
(define (accum op init seqs)
  (if (null? seqs)
      init
      (op (car seqs)
          (accum op init (cdr seqs)))))

=> (accume proc init (x_0 x_1 x_2))
(proc x_0
	(proc x_1 
		(proc x_2 init)))
```
### Left fold
```scheme
(define (accum op init seqs) 
	...)

=> (accume proc init (x_0 x_1 x_2))
(proc 
	(proc 
		(proc init x_0) 
					x_1) 
					 x_2)
```

## filter
```scheme 
(define (filter predicate sequence)  
  (cond ((null? sequence) nil)  
        ((predicate (car sequence))  
         (cons (car sequence)  
               (filter predicate (cdr sequence))))  
        (else (filter predicate (cdr sequence)))))
```

# Extended Interfaces
## accum-n
```scheme
(define (accum-n op init seqs)
  (if (null? (car seqs))
      nil
      (cons (accum op init (map car seqs))
            (accum-n op init (map cdr seqs)))))
```

## mmap
```scheme
(define (mmap op . lists)
  (if (null? (car lists))
      nil
      (cons (apply op (map car lists))
            (apply mmap (cons op (map cdr lists))))))
```