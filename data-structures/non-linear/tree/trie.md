# :heavy_check_mark: Trie
*Last Updated: 1/25/2023*

![Image of a trie](../../../images/data-structures/non-linear/tree/trie.png)

## :round_pushpin: Summary
- Tree-based data structure.
- Stores collection of strings.
- Performs efficient search operations on them.
- Derived from the word, `reTRIEval`.
- If two strings have a common prefix, they will have the same ancestor in the trie.
- Can sort a collection of strings alphabetically.
- Can search whether a string with given prefix is present in the trie or not.

## :round_pushpin: Representation
- Assume only using letters, so 26.
```java
public class TrieNode {
  public TrieNode[] children;
  public int wordCount;

  public TrieNode() {
    children = new TrieNode[26];
    // Number of strings that are stored in the Trie from root to any Trie node.
    wordCount = 0;
  }
}
```

## :round_pushpin: Operations
`N` and `M` represents the size of the string and number of strings that are stored in the trie.
### Insertion
- Time: `O(N)`.
- Space: `O(N * M)`.

### Search
- Time: `O(N)`.
- Space: `O(1)`.

### Deletion
- Time: `O(N)`.
- Space: `O(1)`.

## :round_pushpin: Characteristics
### Advantages
- Can efficiently do `prefix search (or auto-complete)`.
- Print words in alphabetical order.
- No overhead of hash functions in a Trie.
- Searching for a string is done in `O(L)` time, where `L` is the number of words in the query string.

### Disadvantages
- Lots of memory to store all strings.
- A hash table may be faster than a trie.

## :round_pushpin: Properties
- One root node in each Trie.
- Each node of a trie represents a string.
- Each edge represents a character.
- Every node has a hashmap or array of pointers.
  - Each index represents a character and flag indicating end of string.
- Trie can have any number of characters (not just letters).
- Each path from root to any node represents a word or string.

## :round_pushpin: Applications
- Autocomplete Feature.
- Spell Checkers.
- Longest Prefix Matching Algorithm.
