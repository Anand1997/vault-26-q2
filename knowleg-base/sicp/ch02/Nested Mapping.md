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
#todo-pitstop continue with the exercise 
