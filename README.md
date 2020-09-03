# 30-Day-LeetCoding-Challenge-May
### sort+DP BST
### @lru_cache(maxsize=None)
### result = result % (10^9+7)
### TLE: DP ---> scanning/sliding windows (max to min)/while + (l, r) two pointers
### TLE: for loop search ---> binary search
### TLE: deque([]), set()
### TLE: sort() idx and val: greedy
### TLE: pruning
### TLE: list ---> hash (dict)/heap, store min, max, diff, abs, etc.
### TLE: unique: length is important, create a dict/hash based on uniqueness
### TLE: use a priorityQueue,for relaxation of edges:  djikstra's 
### TLE: Kadane's algorithm
### backtracking, recursion, divide and conquer, DP
### check overlapping: if max(left) > min(right)
### reach max depth: keep visiting visited nodes and never exit recursion, go first with the edge cases (can locally freeze some char and change them back)
### tree ---> directed graph (node-based instead of val-based) root, par=None
### tree (i.e. a connected, undirected graph that has no cycles)
### bitmask and hashmap (XOR) keywords: all char count even
### sort list of list, break a tie of sorting
### pair/divisor res = [0]*number of remainders
### if [1,2,3] in list of list
### while(modified in res); for + while
### DAG: in-degree, out-degree; in-flow, out-flow
### mask = 0xFFFFFFFF
1. data structure: stack, queue, deque, tuple, dict, hash, set, heap
   * **lambda sort: list_of_list = sorted(list_of_list, key = lambda x: (-x[0], x[1]))**
   * collections.deque([]), append(), pop(), appendleft(), popleft()
   * list.insert(pos, elements)
   * map(lambda x: x+1, list)
   * ''.join(filter(str.isalnum, s))
   * list.pop(0)
   * queue.popleft()
   * list.append( (key, val) )
   * list.append(tuple)
   * list.pop(index) vs list.remove(value)
   * sorted(temp.items(), reverse = True, key = lambda x: x[1])
   * **heap: heaps O(n log k)**
   * heap: list[0]
   * heapq.heappush(list, item)
   * heapq.heappop(list)
   * heappushpop(list, item)
   * heapq.nsmallest(K, points, lambda (x, y): func), faster than sort
   * {u:i for i, u in enumerate(vocab)}, vocab.items()
   * dict.get()+1 for not-existing pairs
   * all(v >= 0 for v in a.itervalues())
   * **reverse: [::-1]**
   * **remove dict key: my_dict.pop('key', None)**
   * hexadecimals has only 0–9 & A-F/a-f
   * sys.maxsize
   * int(f'{strings:032b}'[::-1],2)
   * s = re.sub(r"[^A-Za-z0-9]", "", s)
   * divisors: idx ** 0.5
   * datetime.strptime(date, "%Y-%m-%d")
   * bisect.bisect_left()
2. collections.Counter(freq), dict, hash, heap, set 
   * Counter(nums).most_common(k)
   * collections.default(list)
   * [[] for _ in range(n)]
   * ex: Graph
3. Bit-wise
   * binary representation and manipulation
   * operations (XOR, OR, AND)
   * bit-wise left shift, 1<<pow, 1<<(pow+1)
   * bit-wise right shifts, pow>>1, (pow+1)>>1
   * rule: sticking 1s from bottom to top, bit[j] vs bit[j-nth-power] has an additional leading 1
   * power of 2 rule: return n > 0 and bin(n).count('1') == 1
   * power of 2 rule: return n > 0 and n & (n-1) == 0
4. BTS/tree (connected graph)
   * index: left = 2*level+1; right = 2*level+2
   * a dummy root, return root.left
   * tree node swap: root.left, root.right = root.right, root.left
   * **curr_node = root = TreeNode(ini_val), return root, curr_node as a pointer to traverse BST**
   * traverse: connect + append temp [] + move pointer
   * left tree: append; 
   * right tree: finish/close traverse, while temp.pop() to implement left --> right
   * is_full(), is_leaf(), get_hight()
   * BST + InOrderTraversal = sorted array
   * BFS/DFS: bfs queue; dfs stack
5. recursion 
   * helper function exit cases return + recursion; initiate inputs + temp{} or existing arrays
   * **ex: Tree Recursion**
   * if parent-children connections, parametrize [] or accu_counters as recursion inputs, else define as a global_variable
   * **nonlocal global_variable**
   * instance variable such as self.global_variable
   * check if the sub-tree can skip the root or not
   * **ex: Routes Connections**
   * graph, valid_roads = set(), visited = [False] * n
   * instance variable self.ans += 1 OR not_valid_roads = set()
   * dfs(node, target)
   * start with nodes connected to target node_0
   * **undirected graph <---> directed graph**
   * **bottom-up tree recursion**
   * **l_ans = dfs(node.left), r_ans = dfs(node.right), return variable (can be a num)**
   * **return variable (can be bool/num) is defined in dfs(node)**
6. DP
   * **base cases check**
   * 2D-DP dynamic counters (top left - bottom right update/search)
   * 2D binary matrix filled with 0's and 1's: DP + accu_counters
   * bottom-right to top-left vs top-left to bottom-right
7. strings
   * "".join(strings).lstrip('0') or '0'
   * int(strings, 2)
   * string += sub_string * freq
   * idx2char, char2idx, ord(), chr()
   * s.startswith()
   * ss.isalpha()
   * strings.count("1")
8. linked list
   * memory
   * self.head = Node()
   * node = curr = head; return node
9. traverse
   * DAG, DFS, SCC, topological sort, stack
   * DAG: in-degree, out-degree; in-flow, out-flow
   * **ex: Course Schedule**
   * for each course, visited = set()
   * while + stack.pop(), DFS/BFS, DP
   * **ignore the first start curr_node**
10. **greedy search and sort**
    * sort is the KEY
    * sort by diff i-j
    * knapsack
### problem summary
11. various scanning/sliding windows problems **[max ---> min]** (min, max, diff, accu_sum, length)
    * **sliding windows** one-pass calc is faster than slicing the array
    * local_min, local_max grid search
    * count for votes +=, -=
    * dynamic append, pop.() and cum-counter++
    * two pointers (l, r) + while loop(s)
    * sum+=, sum-=
    * accu_sum is non-decreasing
    * check diff = target - accu_sum is in temp [] or {}, back track index i
    * **ex: A Contiguous Subarray**
    * **a dummy start, hash {-1:0} or {-1:[0]}**
    * curr_max/curr_min = max/min(curr_max/curr_min, a iterable item)
    * Kadane's algorithm, curr_max, curr_min, tot_max, tot_min, accu_sum rolling
    * **local_max <---> local_min**
    * 26-character dict + rolling counter (hash)
12. some classic problems
    * recursion + exit + temp = [] dynamic append, or self.ans += 1
    * rolling prefix-dict count++
    * LCS, BST + a dummy start, 2D-DP
    * Trie (prefix tree)
    * palindromic, check odd/even lengths
    * subset problems: utilize set A.issubset(B)
    * result = set(); result.add(int(s[i:i+k], 2)) **check len(result)**
    * Fibonacci numbers, cusum
    * **three pointers: for loop i & l = i+1 & r = len(s)-1**
    * **Kadane's algorithm: count submatrices with all ones**
13. any(), all()
    * **once any() returns True and no longer subsequently explores other nodes anymore**
    * **to check all children, use for loop + dfs(), if + self.ans++**
14. DFS (dfs, instance variable, return)
    * top-bottom search: dfs(node) + self.ans + list/set/dict append/add/+=
    * self_or_children_apple |= any(dfs(children) for children in graph[node]
    * **l_ans = dfs(node.left), r_ans = dfs(node.right), return variable (can be a num)**
    * **return variable (can be bool/num) is defined in dfs(node)**
    * dfs(node) + return + self.ans + accum |=
    * visited = set()
    * **2D-grid DFS**: dfs(i, j, idx, stack or count) + can mark "0" as visited, dfs search, and back-track "0" to the original char (static)
15. **palindromic strings: sub-strings/sub-sequences**
    * un-ordered: hash/dict, check odd/even lengths
    * (l, r) two pointers scanning/sliding windows
    * **base cases check (all len(strings) <= 3)**, avoid next step being executed before last step has been computed
    * 2D-DP: if need, for i in range(n-1, -1, -1) for j in range(i, n) check if ss[i] == ss[j]
    * ex: LCS(i=(0,m) and j=(0,n)); LIS(i=(1,n) and j=(0,i)); palindromic(i=(0,n) and j=(i,n))
    * order, index, recursion relation equations, 2D-DP, base cases, sorted()
16. **BST/binary tree/tree/graph**  
    * recursion, divide and conquer (BST)
    * "+" exit 
    * "+" recursion (if or for) left/right/children, l = dfs(node.left), r = dfs(node.right)
    * "+" instance variable 
    * "+" return (recursion/instance variable/may not need)
    * (node is None) is not equal to (not node) !!!
    * degree of tree to node: max(l, r)+1
17. math/permutation
    * math.factorial()
    * math.comb()
    * combinations(range, num_substrings_length) returns all possible combinations
    * chain.from_iterable(combinations())
    * the divisibility test that an integer is divisible by 9 iff the sum of its digits is divisible by 9 (digital root)
    
   
   
   
   





