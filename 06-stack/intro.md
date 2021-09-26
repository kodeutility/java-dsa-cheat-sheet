# Stack
- Stack is a data structure that stores items in a Last-In /First-Out manner (LIFO)
- We can use Stack to reverse the order of occurance since it follows LIFO.
- Java Collection framework provides a Stack class that models and implements a Stack data structure. 
- The class is based on the basic principle of last-in-first-out. 
- In addition to the basic push and pop operations, the class provides three more functions of empty, search, and peek. 
- The class can also be said to extend Vector and treats the class as a stack with the five mentioned functions. The class can also be referred to as the subclass of Vector. 
- Stack can be implemented using Arrays or LinkedList

```java
import java.util.Stack;
// Default initialization of Stack
Stack stack1 = new Stack();

// Initialization of Stack using Generics
Stack<String> stack2 = new Stack<String>();
```

## Stack operations
|Operation|Syntax|
|---|---|
|Create a stack|import java.util.Stack;<br>Stack<E> st = new Stack<E>();|
|Push|st.push("abc");<br>OR<br>st.add("def");|
|Pop|st.pop();|
|Peek|st.peek();|
|isEmpty|st.empty();|
|size|st.size();|
|Print|System.out.println(st);|

## Time and Space Complexity of Stack using LinkedList
|Operation |Time Complexity |Sapce Complexity|
|---|---|---|
|Creating Stack|O(1)|O(1)|
|Push          |O(1)|O(1)|
|Pop           |O(1)|O(1)|
|Peek          |O(1)|O(1)|
|empty         |O(1)|O(1)|
|Delete stack  |O(1)|O(1)|

## Advantages and Disadvantages

### Advantage
- When we want LIFO
- Chance of data corruption is minimum as we can access only top element 

### Disadvantage
- Random access(Index access like arrays) is not possible

