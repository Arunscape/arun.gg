---
{"dg-publish":true,"permalink":"/programming/programming-concepts/queue-data-structure/"}
---

```typescript
type Node<T> = {
  val: T,
  next?: Node<T>,
}

class Queue<T> {
    public length: number;
    private head?: Node<T>;
    private tail?: Node<T>;

    constructor() {
      this.length = 0;
    }

    enqueue(item: T): void {
      const node = {val: item} as Node<T>;
      this.length += 1;
      if (!this.tail) {
        this.tail = this.head = node;
        return;
      }
      this.tail.next = node;
      this.tail = node;
    }

    deque(): T | undefined {
      if (!this.head){
        return undefined;
      }

      this.length -= 1;
      const head = this.head;
      this.head = this.head.next;
      head.next = undefined;
      if (this.length === 0){
        this.tail = undefined
      }

      return head.val;
    }
    peek(): T | undefined {
      return this.head?.val;

    }
}
```
[[programming/programming concepts/FIFO\|FIFO]]
one implementation: use a singly [[programming/programming concepts/linked list\|linked list]]

pop by removing the head

