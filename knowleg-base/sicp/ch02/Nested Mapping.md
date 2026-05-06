- Explains how to loop using #map
```scheme
(accumulate append  
            nil  
            (map (lambda (i)
                   (map (lambda (j) (list i j))  
                        (enumerate-interval 1 (- i 1))))  
                 (enumerate-interval 1 n)))
```
This is one of the extended [[Conventional-Interfaces]]

## Exercise 2.40 
-> pair with no duplicate 

## Exercise 2.41

| Concept    | Tool    |
| ---------- | ------- |
| loops      | flatmap |
| inner loop | map     |
| condition  | filter  |
## Exercise 2.42: 
![[N-Queens]]
 #todo-pitstop 
