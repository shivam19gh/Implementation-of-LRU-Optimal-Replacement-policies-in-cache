# LRU Cache Implementation

## Introduction
This project implements an **LRU (Least Recently Used) Cache** in C++ using a combination of a **doubly linked list** and an **unordered map**. The LRU Cache efficiently handles cache operations such as `get` and `put` with an optimal time complexity of **O(1)**.

---

## Features
- **Efficient Access:** `get` and `put` operations in constant time.
- **Capacity Management:** Automatically evicts the least recently used item when the cache reaches its capacity.
- **Customizable Size:** The cache size can be set during initialization.

---

## How It Works
1. **Doubly Linked List**  
   - Maintains the order of usage with the most recently used item at the head and the least recently used item at the tail.
2. **Unordered Map**  
   - Maps keys to corresponding nodes in the linked list for O(1) access.

### Key Operations:
- **Get:** Retrieves the value of a key and updates its position as the most recently used.
- **Put:** Adds or updates a key-value pair. If the cache is full, the least recently used key is evicted.

---

## Code Structure
- **LRUCache Class**  
   - `addnode(node *newnode)`: Adds a new node right after the head.  
   - `deletenode(node *delnode)`: Removes a node from the linked list.  
   - `get(int key_)`: Fetches the value of the key, updates its position, and returns the value.  
   - `put(int key_, int value)`: Adds/updates a key-value pair, evicting the least recently used item if necessary.  

---

