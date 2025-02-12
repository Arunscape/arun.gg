---
{"dg-publish":true,"permalink":"/programming/programming-concepts/linked-list/"}
---

```
node<T>
	val: T
	next?: Node<T>
	prev?: Node<T> // for a doubly linked list
```

- insertion at a known position is O(1)
- deletion of a known node also constant
- looking up a value (e.g. get the 5th value) is O(n)
- every linked list is a [[tree (data structure)\|tree (data structure)]] and a [[graph (data structure)\|graph (data structure)]]

great for [[programming/programming concepts/queue (data structure)\|queue (data structure)]]