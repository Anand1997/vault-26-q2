# 2.2.1  Representing Sequences

- [ ] #TODO Exercise 2.19
- Exercise 2.20 introduces new lisp syntax and #filter operation.
- After this we are introduced to #map operation.
- Exercise 2.22 explains the difference between **fold-left** and **fold-right** functions 
	- #fold-right recursion
	- #fold-left iteration 
## Recursion Folding 
### #fold-right
❌ Not tail recursive  
❌ Uses stack  
✔ Natural for recursive definitions
### #fold-left
✔ Tail recursive  
✔ Constant space  
✔ Efficient

# 2.2.2  Hierarchical Structures

- Lists with element as list.
- trees and graphs can be represented with this.
- visualize list of list as tree 
- introduce `pair?` and count leaf.
- Exercise 2.24 => draw box-and-point structure.
-  [[2026-04-21]]
- [ ] #TODO Exercise 2.29 
- [x] Exercise 2.30 => `square-tree`  
- [x] Exercise 2.31 => `tree-map`
- [x] Exercise 2.32 => `set-of-subset`
- #todo-pitstop [[2026-04-27]]

# 2.2.3 Sequence as a conventional interface  #todo-current 

- [ ] Exercise 2.33
- [ ] Exercise 2.43