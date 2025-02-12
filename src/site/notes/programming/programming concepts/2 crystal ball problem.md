---
{"dg-publish":true,"permalink":"/programming/programming-concepts/2-crystal-ball-problem/"}
---

### The two crystal ball problem
- given 2 balls that will break if dropped from high enough, determine where it will break
- you could start at 0 and linearly walk up to the point where it breaks
  - but you have 2 balls so you can do better than O(n)
- try jumping sqrt(n) each time with the first ball until it breaks
  - [[O(sqrt(n))\|O(sqrt(n))]]

  
