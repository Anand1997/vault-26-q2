
| #   | Problem                               | Platform                                                                                                                                        | Main Concepts                             |
| --- | ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| 1   | Subsets                               | [LeetCode - Subsets](https://leetcode.com/problems/subsets/?utm_source=chatgpt.com)                                                             | Include/exclude recursion, recursion tree |
| 2   | Permutations                          | [LeetCode - Permutations](https://leetcode.com/problems/permutations/?utm_source=chatgpt.com)                                                   | Visited array, path building              |
| 3   | Combination Sum                       | [LeetCode - Combination Sum](https://leetcode.com/problems/combination-sum/?utm_source=chatgpt.com)                                             | Reusing choices, pruning                  |
| 4   | Generate Parentheses                  | [LeetCode - Generate Parentheses](https://leetcode.com/problems/generate-parentheses/?utm_source=chatgpt.com)                                   | Constraint-based backtracking             |
| 5   | Combination Sum II                    | [LeetCode - Combination Sum II](https://leetcode.com/problems/combination-sum-ii/?utm_source=chatgpt.com)                                       | Duplicate skipping, sorted traversal      |
| 6   | Palindrome Partitioning               | [LeetCode - Palindrome Partitioning](https://leetcode.com/problems/palindrome-partitioning/?utm_source=chatgpt.com)                             | Partition recursion                       |
| 7   | Letter Combinations of a Phone Number | [LeetCode - Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number/?utm_source=chatgpt.com) | Cartesian-product style recursion         |
| 8   | Word Search                           | [LeetCode - Word Search](https://leetcode.com/problems/word-search/?utm_source=chatgpt.com)                                                     | Grid DFS, visited-state backtracking      |
| 9   | N-Queens                              | [LeetCode - N-Queens](https://leetcode.com/problems/n-queens/?utm_source=chatgpt.com)                                                           | Constraint propagation, pruning           |
| 10  | Sudoku Solver                         | [LeetCode - Sudoku Solver](https://leetcode.com/problems/sudoku-solver/?utm_source=chatgpt.com)                                                 | Constraint satisfaction, optimization     |
| 11  | Subsets II                            | [LeetCode - Subsets II](https://leetcode.com/problems/subsets-ii/?utm_source=chatgpt.com)                                                       | Duplicate subset handling                 |
| 12  | Restore IP Addresses                  | [LeetCode - Restore IP Addresses](https://leetcode.com/problems/restore-ip-addresses/?utm_source=chatgpt.com)                                   | Partitioning with validation              |
| 13  | Rat in a Maze                         | [GeeksforGeeks - Rat in a Maze](https://www.geeksforgeeks.org/problems/rat-in-a-maze-problem/1?utm_source=chatgpt.com)                          | Path exploration                          |
| 14  | Beautiful Arrangement                 | [LeetCode - Beautiful Arrangement](https://leetcode.com/problems/beautiful-arrangement/?utm_source=chatgpt.com)                                 | Constraint pruning                        |
| 15  | Expression Add Operators              | [LeetCode - Expression Add Operators](https://leetcode.com/problems/expression-add-operators/?utm_source=chatgpt.com)                           | Recursive expression generation           |
## Problems

[[2026-05-17]] 
#start-sprint 16:59
- [x] 1 Subsets
	- 16:59 start 
	- 17:29 your c\cpp syntax is week , look at the solution and improve it 
	- 17:46 completed the cpp solution , need practice on syntax
	- #todo solve with lisp 
	- 17:47 tracking the recursion on paper
	- 18:23 completed recursion tree => its ugly in procedural language 
	- 18:56 implemented it in lisp sicp style => this is so beautiful
	- #todo-idea a content can be made in comparing both recursion 
- [x] 2 Permutations
	- 19:14 started 
	- 20:35 completed the understanding and implementation of code
	- 20:36 #todo solve the version with the duplicates.
- [x] 3 Combination Sum
	- 21:10 started
	- 21:23 started implementation
	- 21:59 messed up the recursion 
	- 22:03 completed the solution 
	- #todo retrace the recursion
#stop-sprint 22:03
[[2026-05-18]]
#start-sprint 
- [x] 4 Generate Parentheses
	- 20:00 started solving
	- 20:48 done, need more practice on tree pruning
- [x] 5 Combination Sum II
	- 00:08 understood how pruning works
#stop-sprint
- [ ] 6 Palindrome Partitioning
- [ ] 7 Letter Combinations of a Phone Number
- [ ] 8 Word Search
- [ ] 9 N-Queens
- [ ] 10 Sudoku Solver
- [ ] 11 Subsets II
- [ ] 12 Restore IP Addresses
- [ ] 13 Rat in a Maze
- [ ] 14 Beautiful Arrangement
- [ ] 15 Expression Add Operators

---
Tree pruning 
- Stop the recursion at current node
```cpp
void 
backtraking(){
	if(bascase){
		ans.push_back(current);
		return;
	}
	
	// recursion starts here
	// change start to elemente branches 
	for(int idx=start; idx < candidates.size(); idx++){
	
		// pruning 
		if( need to kill branch)
			break; // return also works 
			
		// branch skip to avoid duplicate 
		if(is_duplicate_call)
			continue;
		current.push_back(choic);
		backtracking(...); // add corrent arguments
		current.pop_back();
			
	}
}
```