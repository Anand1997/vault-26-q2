| Layer                | Tool           |
| -------------------- | -------------- |
| element-wise         | `mmap`         |
| reduction            | `accumulate`   |
| structural transform | `accumulate-n` |
| iteration            | `map`          |

we need `mmap` from [[Conventional-Interfaces#Extended Interfaces]]
```scheme 
(define (dot-product v w)  
  (accumulate + 0 (mmap * v w)))

(define (dot-product v w)
  (accum + 0 (mmap * v w)))

(define (transpose mat)
  (accum-n cons nil mat))

(define (matrix-*-vector m v)
  (map (lambda (row) (dot-product row v)) m))

(define (matrix-*-matrix m n)
  (map (lambda (row)
         (map (lambda (col)
                (dot-product row col))
              (transpose n)))
       m))
```

we can rewrite matrix multiplication as follows 
```scheme 
(define (matrix-*-matrix m n)
  (map (lambda (row)
         (matrix-*-vector (transpose n) row))
       m))
```
