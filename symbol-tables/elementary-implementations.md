# Sequential search in a linked list

**Data Structure.** Maintain an \(unsorted\) linked list of key-value pairs.

**Search.** Scan through all keys unitil find a match.

**Insert.** Scan through all keys until find a match; if not match add to front.

**Performannce Summary.**

| ST implementation | worst-case cost\(after N inserts\) |  | average-case\(after N random inserts\) |  | ordered iteration? | key interface |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  | search | insert | search hit | insert |  |  |
| sequential search\(unsorted list\) | N | N | N/2 | N | no | equals\(\) |
| binary search\(orderde array\) | logN | N | logN | N/2 | yes | compareTo\(\) |

**Challenage.** Efficient implementions of both search and insert.

# Binary search in an ordered array

**Data structure.** Maintain an ordered array of key-value pairs.

**Rank helper function. **How many keys &lt; k?

Binary search.

Problem. To insert, need to shift all greater keys over.



