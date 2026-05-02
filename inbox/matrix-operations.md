
we need `mmap` from [[Conventional-Interfaces#Extended Interfaces]]

```scheme 
(define (dot-product v w)  
  (accumulate + 0 (map * v w)))
```