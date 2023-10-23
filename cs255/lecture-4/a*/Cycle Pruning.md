One source of wasted time is expanding nodes in a cycle.

Since checking for cycles in a path of length k is linear in k, we can prune cycles from a path in O(k). There are two methods to resolve this:
- In depth-first methods, checking for cycles can be done in a constant time in path length (e.g., using a hash function)
- For other methods, checking for cycles can be done in linear time in path length