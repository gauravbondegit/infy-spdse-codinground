# Java Sorting 

## 1. Sorting Arrays

| Operation                      | Syntax                                                                                                |
| ------------------------------ | ----------------------------------------------------------------------------------------------------- |
| Sort ascending                 | `Arrays.sort(a);`                                                                                     |
| Sort range `[l, r)`            | `Arrays.sort(a, l, r);`                                                                               |
| Sort descending (`Integer[]`)  | `Arrays.sort(a, Collections.reverseOrder());`                                                         |
| Sort 2D array by first column  | `Arrays.sort(a, (x, y) -> Integer.compare(x[0], y[0]));`                                              |
| Sort 2D array by second column | `Arrays.sort(a, (x, y) -> Integer.compare(x[1], y[1]));`                                              |
| Sort by first, then second     | `Arrays.sort(a, (x, y) -> x[0] != y[0] ? Integer.compare(x[0], y[0]) : Integer.compare(x[1], y[1]));` |
| Binary search (sorted array)   | `Arrays.binarySearch(a, x);`                                                                          |

## 2. Sorting Collections

| Operation                          | Syntax                                                       |
| ---------------------------------- | ------------------------------------------------------------ |
| Sort ArrayList ascending           | `Collections.sort(a);`                                       |
| Sort ArrayList descending          | `a.sort(Collections.reverseOrder());`                        |
| Sort using comparator (asc)              | `a.sort((x, y) -> Integer.compare(x, y));`                   |
| Reverse list                       | `Collections.reverse(a);`                                    |
| Sort strings alphabetically (words = String[])      | `Collections.sort(words);`                                       |
| Sort alphabetically (A-Z) | `Arrays.sort(words);` | Lexicographical order (ASCII: uppercase before lowercase). |
| Sort case-insensitive (A-Z) | `Arrays.sort(words, String.CASE_INSENSITIVE_ORDER);` | Ignores case differences during sorting. |
| Sort strings by length             | `a.sort((x, y) -> Integer.compare(x.length(), y.length()));` |
| Sort list of pairs by first value  | `a.sort((x, y) -> Integer.compare(x.get(0), y.get(0)));`     |
| Sort list of pairs by second value | `a.sort((x, y) -> Integer.compare(x.get(1), y.get(1)));`     |
| Find minimum / maximum             | `Collections.min(a);` / `Collections.max(a);`                |

## 3. Custom Comparator — Most Important

| Requirement                     | Syntax                                                                                  |
| ------------------------------- | --------------------------------------------------------------------------------------- |
| Ascending                       | `(x, y) -> Integer.compare(x, y)`                                                       |
| Descending                      | `(x, y) -> Integer.compare(y, x)`                                                       |
| Sort by object field            | `a.sort((x, y) -> Integer.compare(x.val, y.val));`                                      |
| Sort by descending field        | `a.sort((x, y) -> Integer.compare(y.val, x.val));`                                      |
| Tie-break by second field       | `a.sort((x, y) -> x.a != y.a ? Integer.compare(x.a, y.a) : Integer.compare(x.b, y.b));` |
| Using `Comparator.comparingInt` | `a.sort(Comparator.comparingInt(x -> x.val));`                                          |
| Reverse comparator              | `a.sort(Comparator.comparingInt((Item x) -> x.val).reversed());`                        |

## 4. Sorting PriorityQueue

| Requirement          | Syntax                                                                                                                               |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| Min-Heap             | `PriorityQueue<Integer> pq = new PriorityQueue<>();`                                                                                 |
| Max-Heap             | `PriorityQueue<Integer> pq = new PriorityQueue<>(Collections.reverseOrder());`                                                       |
| Pair by first value  | `PriorityQueue<int[]> pq = new PriorityQueue<>((x, y) -> Integer.compare(x[0], y[0]));`                                              |
| Pair by second value | `PriorityQueue<int[]> pq = new PriorityQueue<>((x, y) -> Integer.compare(x[1], y[1]));`                                              |
| Pair with tie-break  | `PriorityQueue<int[]> pq = new PriorityQueue<>((x, y) -> x[0] != y[0] ? Integer.compare(x[0], y[0]) : Integer.compare(x[1], y[1]));` |
                                
## 5. Essential Rules

| Rule                         | Remember                                                                      |
| ---------------------------- | ----------------------------------------------------------------------------- |
| Primitive array `int[]`      | `Arrays.sort(a);`                                                             |
| Object array `Integer[]`     | Supports comparator sorting                                                   |
| `ArrayList<Integer>`         | `Collections.sort(a);` or `a.sort(...)`                                       |
| 2D primitive array `int[][]` | Supports comparator sorting                                                   |
| `HashMap` / `HashSet`        | No guaranteed sorted iteration order                                          |
| `TreeMap` / `TreeSet`        | Automatically maintain sorted order                                           |
| `PriorityQueue`              | Only the head is guaranteed to have highest priority; iteration is not sorted |
| Comparator safety            | Prefer `Integer.compare(x, y)` over `x - y`                                   |
