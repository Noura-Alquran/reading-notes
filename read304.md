# Reading : Hash-tables summary :
* **What is a Hashtable?**
*  **hash table (hash map)** is a data structure that implements an associative array abstract data type, a structure that can map **keys** to **values**(This means every Node or Bucket has both a key, and a value). A hash table uses a hash function to compute an index, also called a hash code, into an array of buckets or slots, from which the desired value can be found. During lookup, the key is hashed and the resulting hash indicates where the corresponding value is stored.

* **Terminology** :
 1. **Hash** - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. *In the case of a hashtable, it is used to determine the index of the array.*
 2. **Buckets** - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a **collision** occurs.
 3. **Collisions** - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

* **Why do we use them?**
 - Hold unique values
 - Dictionary
 - Library 

* Hash maps take advantage of an array’s O(1) read access. Instead of adding elements to an array from beginning to end, a hash map uses a “hash function” to place each item at a precise index location, based off it’s key.
* A hashtable traditionally is created from an array.After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:
1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.
* The worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.

* Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a LinkedList in each one ,Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. Each index in the array is called a **“bucket”** because it can store multiple key/value pairs.
* Hash maps do this to store values:
    * accept a key
    * calculate the hash of the key
    * use modulus to convert the hash into an array index.
    * store the key with the value by appending both to the end of a linked list
* Hash maps do this to read value:
    * accept a key
    * calculate the hash of the key
    * use modulus to convert the hash into an array index
    * use the array index to access the short LinkedList representing a bucket
    * search through the bucket looking for a node with a key/value pair that matches the key you were given

* **Recognize**: calculating load factors and choosing the optimal number of buckets, and determining the best hash functions is not within the scope of this class. This class intends to introduce you to what a hash table is, how it’s implemented, what hash codes are, how to handle collisions and how to reason generally about what it means for a hash table to be more empty or more full. This class does not intend to calculate theoretical optimal performance limits for how to best balance a Hash Table.
* **Internal Methods**
1. Add(): When adding a new key/value pair to a hashtable:
    - send the key to the GetHash method.
    - Once you determine the index of where it should be placed, go to that index
    - Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
    If something does exist, add the new key/value pair to the data structure within that bucket.
2. Find(): The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.
3. Contains() : The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.
4. GetHash(): The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

