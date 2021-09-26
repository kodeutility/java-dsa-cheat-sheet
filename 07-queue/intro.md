# Queue
- Queue is a data structure that stores items in a First-In /First-Out manner (FIFO)
- Utilize first incoming data first, while others wait for their turn
- Java Collection framework provides a Queue class that models and implements a Queue data structure. 
- Queue can be implemented using Arrays or LinkedList

### Implementation
1. Array
    - Linear Queue
    - Circular Queue
2. Linked List

```java
import java.util.Queue;
import java.util.LinkedList;

// Initialization of Queue using Generics
Queue<String> queue2 = new LinkedList<String>();
```

## Queue operations
|Operation|Syntax|
|---|---|
|Create a Queue|import java.util.Queue;<br>import java.util.LinkedList;<br>Queue<E> q = new LinkedList<E>();|
|Enqueue(add element to queue)|q.add("def");<br>q.offer("def");|
|Poll(remove first element)|q.poll();<br>q.remove();|
|Peek|q.peek();<br>q.element();|
|contains|q.contains("abc");|
|size|q.size();|
|Delete all elements|q.clear();|
|Print|System.out.println(q);|
|Convert to array|q.toArray();<br>q.toArray()[1];|

|Operation|Throws exception|Special value|
|---|---|---|
|Insert|add(e)|offer(e)|
|Remove|remove()|poll()|
|Examine|element()|peek()|

## Time and Space Complexity of Queue using LinkedList
|Operation |Time Complexity |Sapce Complexity|
|---|---|---|
|Creating Queue|O(1)|O(1)|
|Push          |O(1)|O(1)|
|Pop           |O(1)|O(1)|
|Peek          |O(1)|O(1)|
|empty         |O(1)|O(1)|
|Delete Queue  |O(1)|O(1)|

## Advantages and Disadvantages

### Advantage
- When we want FIFO
- Chance of data corruption is minimum as we can access only top element 

### Disadvantage
- Random access(Index access like arrays) is not possible