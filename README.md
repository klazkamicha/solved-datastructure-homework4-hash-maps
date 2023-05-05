Download Link: https://assignmentchef.com/product/solved-datastructure-homework4-hash-maps
<br>
<h1>Hash Maps</h1>

In this homework, you will implement a key-value hash map with a linear probing collision resolution strategy. A hash map maps keys to values and allows <em>O</em>(1) average case lookup of a value when the key is known. This hash map must be resized to have a capacity of 2<em>n </em>+ 1 where <em>n </em>is the current capacity when the table exceeds (greater than, not greater than or equal to) the max load factor provided in HashMap.java

The table <strong>should not add duplicate keys</strong>, but duplicate values are acceptable. In the event of a duplicate key, replace the existing value with the new value.

There are two constructors in HashMap.java. As per the javadocs, you should use constructor chaining to implement the no-arg constructor.

<h2>Hash Functions</h2>

You should not write your own hash functions for this assignment; use the hashCode() method (every Object has one). If this is a negative value, mod by table length first, then take the absolute value (it must be done in this order to prevent overflow in certain cases).

<h2>Linear Probing</h2>

Your hash map must implement a linear probing collision policy. If the hash value of the key is occupied, probe in linear increments. For example, if the hash value of your key is 7 with a backing array of capacity 9, and index 7 in the array is occupied, check index 7+1 mod 9, then 7+2 mod 9, then 7+3 mod 9, etc.

<h2>Adding Items</h2>

When adding a key/value pair to a hash map, add the pair to the array in the correct position. Also remember that keys are unique in a hash map, so you must ensure that duplicate keys are not added.

<h2>Removing Items</h2>

Since linear probing is an open addressing scheme, you cannot set removed entries to null. Instead, you need to implement a ”soft remove” using the removed flag in MapEntry.java. Keep in mind that all the flag does is provide a way to keep track what entries have been removed, but you need to implement the logic for what to do with the removed entries. Though the objects may still be in memory, as far as the user is concerned, the data has been removed, and your code’s behavior should reflect this expectation.