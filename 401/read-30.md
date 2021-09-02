# Hash Tables

## Intro to Hash Tables
**What is a Hashtable?**
- Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose, it is used to determine the index of the array. 
- Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket.
- Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.
**Internal Methods**
1. `Add()`: adds a new key/value pair to a hashtable.
2. `Find()`:  takes in a key, gets the Hash, and goes to the index location specified. 
3. `Contains()`: will accept a key, and return a bool on if that key exists inside the hashtable. 
4. `GetHash()`: will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

## Basics of Hash Tables
Hashing is a technique that is used to uniquely identify a specific object from a group of similar objects. Some examples of how hashing is used in our lives include:

- In universities, each student is assigned a unique roll number that can be used to retrieve information about them.
- In libraries, each book is assigned a unique number that can be used to determine information about the book.

* Hashing is implemented in two steps:
1. An element is converted into an integer by using a hash function. This element can be used as an index to store the original element, which falls into the hash table.
2. The element is stored in the hash table where it can be quickly retrieved using hashed key.

**Applications**
1. Associative arrays.
2. Database indexing.
3. Caches.
4. Object representation.