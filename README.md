# 30-Day-LeetCoding-Challenge-May
### data structure: stack, queue, deque, tuple, dict, hash, set, heap
### @lru_cache(maxsize=None)
### graph
1. Counter, dict, hash
2. Bit-wise
   * binary representation and manipulation
   * operations (XOR, OR, AND)
   * shifts*2, 1<<pow, 1<<(pow+1)
   * shifts/2, pow>>1, (pow+1)>>1
   * rule: sticking 1s from bottom to top, bit[j] vs bit[j-nth-power] has an additional leading 1
3. Binary Tree Search
   * a dummy root, return root.left
   * curr_node = root = TreeNode(ini_val), return root, curr_node as a pointer to traverse BST
   * traverse: connect + append temp [] + move pointer
   * left tree: append; 
   * right tree: finish/close traverse, while temp.pop() to implement left --> right
   * is_full(), is_leaf(), get_hight()
4. Recursion (helper function exit cases return + recursion; initiate inputs + temp{} or existing arrays)
   * ex: **tree recursion**
   * if parent-children connections, parametrize [] or accu_counters as recursion inputs, else define as a global_variable
   * **nonlocal global_variable**
   * self.global_variable
   * check if the sub-tree can skip the root or not
   * ex: **routes connections**
   * graph, valid_roads = set(), visited = [False] * n
   * instance variable self.ans += 1 OR not_valid_roads = set()
   * dfs(node, target)
   * start with nodes connected to target node_0
   * **undirected graph <---> directed graph**
   * **bottom-up tree recursion**
   * dfs(root, root.left) + dfs(root, root.right), **recursion first**
   * **return variable (can be bool) is defined in dfs(node)**
5. Count for votes +=, -=
6. "".join(strings).lstrip('0') or '0'
7. Dynamic append, pop.() and cum-counter++
8. all(v >= 0 for v in a.itervalues())
9. Trie (prefix tree)
10. Kadane's algorithm, curr_max, curr_min, tot_max, tot_min, accu_sum rolling
11. Linked list
12. 26-character dict + rolling counter (hash)
13. append( (key, val) )
14. BST + InOrderTraversal = sorted array
15. 2D-DP dynamic counters
16. sorted(temp.items(), reverse = True, key = lambda x: x[1])
17. string += sub_string * freq
18. {u:i for i, u in enumerate(vocab)}, vocab.items()
19. dict.get()+1 for not-existing pairs
20. Two pointers (l, r) + while loop(s)
    * sum+= sum-=
    * accu_sum is non-decreasing
    * check diff = target - accu_sum is in temp [] or {}, back track index i
    * **a contiguous subarray**
    * a dummy start, hash {-1:0} or {-1:[0]}
    * curr_max/curr_min = max/min(curr_max/curr_min, a iterable item)
21. idx2char, char2idx, ord()
22. LCS, BST + a dummy start, 2D-DP
23. BFS/DFS: bfs queue; dfs stack
24. DAG, DFS, SCC, topological sort, stack
    * ex: **Course Schedule**
    * graph: collections.defaultdict(list), [course and all paired nxt] (including []), or dict{}
    * for each course, visited = set()
    * while + stack.pop(), DFS/BFS, DP
    * **ignore the first start curr_node**
25. result = set(); result.add(int(s[i:i+k], 2)) **check len(result)**
26. palindromic, check odd/even lengths
27. any(), all()
    * self_or_children_apple |= any(dfs(children) for children in graph[node])
    * **once any() returns True and no longer subsequently explores other nodes anymore**
    * **to check all children, use for loop + dfs(), if + self.ans++**
28. list.pop(0)
29. heap: heaps O(n log k)
    * heapq.nsmallest(K, points, lambda (x, y): func), faster than sort
30. 2D binary matrix filled with 0's and 1's: DP + accu_counters
31. queue.popleft()
32. **result = result % (10^9+7)**
33. **greedy search**
    * sort by diff i-j
34. list.pop(index) vs list.remove(value)
35. subset problems: utilize set A.issubset(B)









