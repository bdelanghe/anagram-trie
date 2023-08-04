# 🧩 Anagram Trie

Anagram Trie is a project that leverages the data structure of Trie to effectively solve anagrams in Python.

The code uses a Trie data structure to store words where each path from the root to a leaf node represents a word. This way, we can efficiently perform operations like checking if a word exists in the trie or retrieving anagrams of a given word.

The implementation makes use of Python's powerful data science libraries including `dataclasses`, `typing`, `collections` and `json`.

## 📝 Code Overview

The `Node`, `Leaf` and `VectorTrie` classes form the backbone of our Trie structure. 

- `Node` class serves as the building block for our Trie structure, representing a single character and keeping a reference to its child nodes.
- `Leaf` class is a representation of the end of a word.
- `VectorTrie` class contains the functionality for the Trie data structure, including methods for adding words to the Trie (`add_word`, `add_words`), checking if a word is in the Trie (`check_word`) and retrieving all anagrams of a given word (`get_words`).

## 💻 Usage

This project is designed to be used in a Jupyter notebook environment. Here's a basic usage example:

```python
trie = VectorTrie()
trie.add_word('aba')  # Add a word to the Trie
trie.check_word('aba')  # Check if a word is in the Trie
trie.get_words('aba')  # Get anagrams of a given word
```

Also, words can be added from a json file using the `add_words` function:

```python
with open('words.json', 'r') as f:
    trie.add_words(json.load(f))
```

## 📜 License

This project is open source and available under the MIT License.
