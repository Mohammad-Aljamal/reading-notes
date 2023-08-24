# Class 30


# Hash Tables


## What is a Hashtable?
A hash table is a type of data structure that uses an array and linked lists to to store data. We can split the defenition of a hash table into three Terminologies:

1.Hash: the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

2.Buckets: it's what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

3.Collisions: it's what happens when more than one key gets hashed to the same location of the hashtable.

## Creating a Hash
Here is a simplistic hashing algorithm:

1.Add or multiply all the ASCII values together.

2.Multiply it by a prime number such as 599.

3.Use modulo to get the remainder of the result, when divided by the total size of the array.

4.Insert into the array at that index.

## Collisions
A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.

If two keys ever ultimately resolved to the same index, then two calls to .Add(key, val) with different keys would overwrite each other.

Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a LinkedList in each one! Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. Each index in the array is called a “bucket” because it can store multiple key/value pairs.

## Methods
#### set()
send the key to the hash() method.
2.Once you determine the index of where it should be placed, go to that index

3.Check if something exists at that index already, if it doesn’t, add it with the key/value pair.

4.If something does exist, add the new key/value pair to the data structure within that bucket.

#### hash()
The hash() method will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

#### keys()
The keys() method returns a collection (array) of unique hash keys.

#### has()
The has() method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the hash() method and check the hashtable if the key exists in the table given the index returned.

### get()
The get() method takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.



## Resources

## [Read Intro to Hash Tables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
## [Watch what is a hash table?](https://www.youtube.com/watch?v=MfhjkfocRR0)
## [Read basics of hash tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)
## [Skim hash table wiki](https://en.wikipedia.org/wiki/Hash_table)
