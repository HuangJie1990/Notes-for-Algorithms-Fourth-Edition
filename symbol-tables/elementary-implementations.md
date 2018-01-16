# Sequential search in a linked list



**Data Structure.** Maintain an \(unsorted\) linked list of key-value pairs.

**Search.** Scan through all keys unitil find a match.

**Insert.** Scan through all keys until find a match; if not match add to front.

**Performannce Summary.**

| worst-case cost\(after N inserts\) |  | average-case\(after N random inserts\) |  | ordered iteration? | key interface |
| :---: | :---: | :---: | :---: | :---: | :---: |
| search | insert | search hit | insert |  |  |
| N | N | N/2 | N | no | equals\(\) |

**Challenage.** Efficient implementions of both search and insert.

