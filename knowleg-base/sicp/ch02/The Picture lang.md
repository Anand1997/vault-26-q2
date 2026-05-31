- This needs racket 
	- https://docs.racket-lang.org/sicp-manual/SICP_Picture_Language.html

```scheme 
(require sicp-pict)
(paint (number->painter 0))
(paint diagonal-shading)
(paint (below (beside diagonal-shading
                (rotate90 diagonal-shading))
         (beside (rotate270 diagonal-shading)
                 (rotate180 diagonal-shading))))
(paint einstein)
```
#TODO skipped for now
- not Very interesting 