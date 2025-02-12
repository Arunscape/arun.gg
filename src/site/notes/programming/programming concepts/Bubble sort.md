---
{"dg-publish":true,"permalink":"/programming/programming-concepts/bubble-sort/"}
---

[[sorting algorithms\|sorting algorithms]]
- move largest number to end
  - move second largest to second last
    - ...continue
- [[Gauss\|Gauss]]: sum of numbers in range (1..=n) is n(n+1)/2
$$
	\sum_{i=1}^n i = \frac{n(n+1)}{2}
$$
- [[O(n^2)\|O(n^2)]]


```typescript
function bubble_sort(arr: number[]): void {
  let tmp;
  for (let i=0; i < arr.length; i+=1){
    for (let j=0; j < arr.length - 1 - i; j+=1){
      if (arr[j+1] < arr[j]){
        tmp = arr[j];
        arr[j] = arr[j+1];
        arr[j+1] = tmp;
      }
    }
  }
}

```