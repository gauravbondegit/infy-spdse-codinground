
# Java Arrays & 2D Matrix

### 1. Array Operations

| Operation | Syntax |
| :--- | :--- |
| Create array | `int[] a = new int[n];` |
| Initialize array | `int[] a = {1, 2, 3};` |
| Get element | `a[i];` |
| Update element | `a[i] = x;` |
| Length | `a.length;` |
| Sort ascending | `Arrays.sort(a);` |
| Sort range `[l, r)` | `Arrays.sort(a, l, r);` |
| Binary search (sorted array) | `Arrays.binarySearch(a, x);` |
| Fill array | `Arrays.fill(a, -1);` |
| Copy array | `int[] b = Arrays.copyOf(a, a.length);` |
| Copy range `[l, r)` | `int[] b = Arrays.copyOfRange(a, l, r);` |
| Compare arrays | `Arrays.equals(a, b);` |
| Convert to string | `Arrays.toString(a);` |
| Minimum / maximum | `Math.min(x, y);` / `Math.max(x, y);` |
| Swap elements | `int t = a[i]; a[i] = a[j]; a[j] = t;` |

### 2. Array Traversal

| Operation | Syntax |
| :--- | :--- |
| Normal `for` loop | `for (int i = 0; i < a.length; i++) { int x = a[i]; }` |
| Enhanced `for` loop | `for (int x : a) { }` |
| Two pointers | `int l = 0, r = a.length - 1; while (l < r) { }` |


### 3. 2D Array / Matrix Operations

| Operation | Syntax |
| :--- | :--- |
| Create matrix | `int[][] a = new int[m][n];` |
| Initialize matrix | `int[][] a = {{1, 2}, {3, 4}};` |
| Get cell | `a[i][j];` |
| Update cell | `a[i][j] = x;` |
| Number of rows | `a.length;` |
| Number of columns | `a[0].length;` |
| Row traversal | `for (int i = 0; i < a.length; i++) { }` |
| Column traversal | `for (int j = 0; j < a[0].length; j++) { }` |

# ArrayList 

| Operation | Syntax |
| :--- | :--- |
| Create empty list | `List<Integer> a = new ArrayList<>();` |
| Add element | `a.add(x);` |
| Insert at index | `a.add(i, x);` |
| Get element | `a.get(i);` |
| Update element | `a.set(i, x);` |
| Remove by index | `a.remove(i);` |
| Remove by value | `a.remove(Integer.valueOf(x));` |
| Size | `a.size();` |
| Check empty | `a.isEmpty();` |
| Check membership | `a.contains(x);` |
| Find index | `a.indexOf(x);` |
| Clear list | `a.clear();` |
| Convert to array | `a.toArray(new Integer[0]);` |
| Sort integers ascending | `Collections.sort(a);` |
| Custom sorting | `a.sort((x, y) -> Integer.compare(x, y));` |
| Normal for loop | `for (int i = 0; i < a.size(); i++) { int x = a.get(i); }` |
| Enhanced for loop | `for (int x : a) { System.out.println(x); }` |

## Nested Lists (List of Lists)

| Operation | Syntax |
| :--- | :--- |
| Declaration | `List<List<Integer>> adj = new ArrayList<>();` |
| Add initialized list (mutable) | `adj.add(new ArrayList<>(Arrays.asList(1, 2, 3)));` |
| Add new empty list | `adj.add(new ArrayList<>());` |
| Add deep copy (Backtracking/Subsets) | `adj.add(new ArrayList<>(currList));` |
| Add element to inner list at index `i` | `adj.get(i).add(val);` |
| Get element at `(r, c)` | `adj.get(r).get(c);` |
| Update element at `(r, c)` | `adj.get(r).set(c, val);` |
| Size of outer / inner list | `adj.size();` / `adj.get(r).size();` |
| 2D Traversal (Nested loop) | `for (List<Integer> row : adj) { for (int x : row) { } }` |

# Java String 

### Basic Operations

| Operation | Syntax |
| :--- | :--- |
| Create string | `String s = "hello";` |
| Get length | `s.length();` |
| Get character | `s.charAt(i);` |
| Get substring [l, r) | `s.substring(l, r);` |
| Get substring from index | `s.substring(i);` |
| Find character/string | `s.indexOf("a");` |
| Find last occurrence | `s.lastIndexOf("a");` |
| Check containment | `s.contains("abc");` |
| Check empty | `s.isEmpty();` |
| Compare strings | `s.equals(t);` |
| Compare ignoring case | `s.equalsIgnoreCase(t);` |
| Lexicographic comparison | `s.compareTo(t);` |
| Check prefix | `s.startsWith("ab");` |
| Check suffix | `s.endsWith("xy");` |

### Modification and Conversion

| Operation | Syntax |
| :--- | :--- |
| Convert to lowercase | `s.toLowerCase();` |
| Convert to uppercase | `s.toUpperCase();` |
| Remove leading/trailing spaces | `s.trim();` |
| Replace character | `s.replace('a', 'b');` |
| Replace substring | `s.replace("ab", "xy");` |
| Split into strings | `s.split(" ");` Result (String[])|
| Split by 1+ whitespaces (Safe) | `s.trim().split("\\s+");` Result (String[])|
| String to character array | `s.toCharArray();` |
| String to integer | `Integer.parseInt(s);` |
| Integer to string | `String.valueOf(n);` |
| Character to string | `String.valueOf(c);` |
| Character digit to integer | `c - '0'` |
| Integer digit to character | `(char) (n + '0')` |

### Traversal

| Operation | Syntax |
| :--- | :--- |
| Normal for loop | `for (int i = 0; i < s.length(); i++) { char c = s.charAt(i); }` |
| Reverse for loop | `for (int i = s.length() - 1; i >= 0; i--) { char c = s.charAt(i); }` |
| Enhanced for loop | `for (char c : s.toCharArray()) { }` |

### StringBuilder

| Operation | Syntax |
| :--- | :--- |
| Create | `StringBuilder sb = new StringBuilder();` |
| Initialize from string | `StringBuilder sb = new StringBuilder(s);` |
| Append character/string | `sb.append(c);` |
| Get character | `sb.charAt(i);` |
| Update character | `sb.setCharAt(i, c);` |
| Delete character at index | `sb.deleteCharAt(i);` |
| Delete range [l, r) | `sb.delete(l, r);` |
| Clear builder | `sb.setLength(0);` |
| Reverse | `sb.reverse();` |
| Length | `sb.length();` |
| Convert to string | `sb.toString();` |
| Insert at index | `sb.insert(i, c);` |
| Replace range [l, r) | `sb.replace(l, r, "abc");` |

### Character Checks

| Operation | Syntax |
| :--- | :--- |
| Is letter | `Character.isLetter(c)` |
| Is digit | `Character.isDigit(c)` |
| Is alphanumeric | `Character.isLetterOrDigit(c)` |
| Is uppercase | `Character.isUpperCase(c)` |
| Is lowercase | `Character.isLowerCase(c)` |
| Convert to lowercase | `Character.toLowerCase(c)` |
| Convert to uppercase | `Character.toUpperCase(c)` |

# Java HashMap Cheat Sheet 

### Basic Operations

| Operation | Syntax |
| :--- | :--- |
| Create HashMap | `Map<Integer, Integer> mp = new HashMap<>();` |
| Insert / Update | `mp.put(k, v);` |
| Get value | `mp.get(k);` |
| Get value with default | `mp.getOrDefault(k, 0);` |
| Check key exists | `mp.containsKey(k);` |
| Check value exists | `mp.containsValue(v);` |
| Remove key | `mp.remove(k);` |
| Map size | `mp.size();` |
| Check empty | `mp.isEmpty();` |
| Clear map | `mp.clear();` |

### Frequency Counting

| Operation | Syntax |
| :--- | :--- |
| Count frequency | `mp.put(x, mp.getOrDefault(x, 0) + 1);` |
| Decrease frequency | `mp.put(x, mp.get(x) - 1);` |
| Remove if frequency becomes zero | `if (mp.get(x) == 0) mp.remove(x);` |
| Initialize missing key | `mp.putIfAbsent(k, v);` |

### Traversal

| Operation | Syntax |
| :--- | :--- |
| Traverse keys | `for (int k : mp.keySet()) { }` |
| Traverse values | `for (int v : mp.values()) { }` |
| Traverse key-value pairs | `for (Map.Entry<Integer, Integer> e : mp.entrySet()) { int k = e.getKey(); int v = e.getValue(); }` |

# Java HashSet Cheat Sheet 

### Basic Operations

| Operation | Syntax |
| :--- | :--- |
| Create HashSet | `Set<Integer> set = new HashSet<>();` |
| Add element | `set.add(x);` |
| Remove element | `set.remove(x);` |
| Check element exists | `set.contains(x);` |
| Set size | `set.size();` |
| Check empty | `set.isEmpty();` |
| Clear set | `set.clear();` |
| Add only if absent | `set.add(x);` |
| Copy a set | `Set<Integer> b = new HashSet<>(set);` |

### Traversal

| Operation | Syntax |
| :--- | :--- |
| Enhanced for loop | `for (int x : set) { }` |

### Set Operations

| Operation | Syntax |
| :--- | :--- |
| Union | `set.addAll(b);` |
| Intersection | `set.retainAll(b);` |
| Difference (`set - b`) | `set.removeAll(b);` |
| Check subset (b is subset of set) | `b.containsAll(set);` |
| Convert list to set | `Set<Integer> set = new HashSet<>(list);` |
| Convert set to list | `List<Integer> list = new ArrayList<>(set);` |

# Java Stack Cheat Sheet 

### Basic Operations (`Stack<Integer>`)

| Operation | Syntax |
| :--- | :--- |
| Create stack | `Stack<Integer> st = new Stack<>();` |
| Push element | `st.push(x);` |
| Pop top element | `st.pop();` |
| Peek top element | `st.peek();` |
| Check empty | `st.isEmpty();` |
| Stack size | `st.size();` |
| Search element (1-based from top) | `st.search(x);` |
| Check top element | `st.peek() == x` |
| Clear stack | `st.clear();` |

### Traversal and Access

| Operation | Syntax |
| :--- | :--- |
| Traverse bottom to top | `for (int x : st) { }` |
| Traverse top to bottom | `for (int i = st.size() - 1; i >= 0; i--) { int x = st.get(i); }` |
| Access element by index | `st.get(i);` |

### Essential Safety Checks

| Operation | Syntax |
| :--- | :--- |
| Check before popping | `if (!st.isEmpty()) st.pop();` |
| Check before peeking | `if (!st.isEmpty()) st.peek();` |
| Check top element | `!st.isEmpty() && st.peek() == x` |

### Recommended Stack (`ArrayDeque`)

| Operation | Syntax |
| :--- | :--- |
| Create stack | `Deque<Integer> st = new ArrayDeque<>();` |
| Push | `st.push(x);` |
| Pop | `st.pop();` |
| Peek | `st.peek();` |
| Check empty | `st.isEmpty();` |
| Size | `st.size();` |
| Safe pop | `if (!st.isEmpty()) st.pop();` |
| Safe peek | `if (!st.isEmpty()) st.peek();` |

# Java Queue Cheat Sheet 

### Basic Operations (`Queue`)

| Operation | Syntax |
| :--- | :--- |
| Create queue | `Queue<Integer> q = new LinkedList<>();` |
| Add element | `q.offer(x);` |
| Add element (throws exception on failure) | `q.add(x);` |
| Remove front element | `q.poll();` |
| Get front element | `q.peek();` |
| Queue size | `q.size();` |
| Check empty | `q.isEmpty();` |
| Check element exists | `q.contains(x);` |
| Clear queue | `q.clear();` |

### Traversal

| Operation | Syntax |
| :--- | :--- |
| Enhanced for loop | `for (int x : q) { }` |
| Iterate and print | `for (int x : q) System.out.println(x);` |
| Remove all elements | `while (!q.isEmpty()) { int x = q.poll(); }` |

### Deque (`ArrayDeque`)

| Operation | Syntax |
| :--- | :--- |
| Create deque | `Deque<Integer> q = new ArrayDeque<>();` |
| Insert at front | `q.offerFirst(x);` |
| Insert at rear | `q.offerLast(x);` |
| Remove from front | `q.pollFirst();` |
| Remove from rear | `q.pollLast();` |
| Get front | `q.peekFirst();` |
| Get rear | `q.peekLast();` |
| Size | `q.size();` |
| Check empty | `q.isEmpty();` |

# Java PriorityQueue Cheat Sheet 

PriorityQueue = Binary Heap. Elements are ordered by priority rather than insertion sequence. Java defaults to a Min-Heap (smallest element first). Use a Max-Heap when the largest element should take priority.


### 1. Creation

| Operation | Syntax |
| :--- | :--- |
| Min-Heap (Default) | `PriorityQueue<Integer> pq = new PriorityQueue<>();` |
| Max-Heap | `PriorityQueue<Integer> pq = new PriorityQueue<>(Collections.reverseOrder());` |
| Custom comparator | `PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> Integer.compare(a[0], b[0]));` |
| Initialize from collection | `PriorityQueue<Integer> pq = new PriorityQueue<>(list);` |


### 2. Basic Operations

| Operation | Syntax |
| :--- | :--- |
| Insert element (Preferred) | `pq.offer(x);` |
| Insert element | `pq.add(x);` |
| Get top element | `pq.peek();` |
| Remove top element | `pq.poll();` |
| Remove specific element | `pq.remove(x);` |
| Check element exists | `pq.contains(x);` |
| Size | `pq.size();` |
| Check empty | `pq.isEmpty();` |
| Clear queue | `pq.clear();` |

### 3. Traversal and Conversion

| Operation | Syntax |
| :--- | :--- |
| Process in priority order | `while (!pq.isEmpty()) { int x = pq.poll(); }` |
| Unordered iteration (Do NOT use for sorted order) | `for (int x : pq) { }` |
| Copy heap | `PriorityQueue<Integer> copy = new PriorityQueue<>(pq);` |
| Convert to array (Unordered) | `pq.toArray();` |

### 4. Custom Heaps (Pairs & Coordinates)

| Requirement | Syntax |
| :--- | :--- |
| Min-Heap of pairs by first value | `PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> Integer.compare(a[0], b[0]));` |
| Max-Heap of pairs by first value | `PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> Integer.compare(b[0], a[0]));` |
| Sort by second value | `PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> Integer.compare(a[1], b[1]));` |
| Tie-break by second value | `PriorityQueue<int[]> pq = new PriorityQueue<>((a, b) -> a[0] != b[0] ? Integer.compare(a[0], b[0]) : Integer.compare(a[1], b[1]));` |
| Store pair | `pq.offer(new int[]{x, y});` |
| Extract pair | `int[] a = pq.poll(); int x = a[0], y = a[1];` |

| Pattern | Strategy & Syntax |
| :--- | :--- |
| **Top K Largest** | Use Min-Heap of size $K$:<br>`PriorityQueue<Integer> pq = new PriorityQueue<>();`<br>`pq.offer(x);`<br>`if (pq.size() > k) pq.poll();` |

