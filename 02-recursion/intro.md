# Recursion

- A way of solving problem by having a function calling itself
- Performing the same operation multiple times
- In every step we try smaller input to make the problem smaller
- Base condition is needed to stop the recursion, otherwise it will become infinite loop

### When to choose recursion?
- If we can divide the problem into similar sub problems
- Design an algorithm to compute nth...
- Write code to list n...
- Implement a method to compute all
- Mainly used in trees and graphs
- Used in divide and conquer, dynamic programming
- When we use memoization
- When we are ok with the time and space being not efficient


### When not to use recursion?
- If time and space complexity matters

### How it works?
- Similar to below code
```java
static void firstMethod(){
    secondMethod();
    System.out.println("First method");
}

static void secondMethod(){
    thirdMethod();
    System.out.println("Second method");
}

static void thirdMethod(){
    fourthMethod();
    System.out.println("Third method");
}

static void fourthMethod(){
    // This acts as base case
    System.out.println("Fourth method");
}
```
- on every function call, current operation is paused and next function call is executed by adding it top of stack memory
- Once the execution of function is completed it is removed from the stack memory

### Recursive vs Iterative Solutions
- Any problems which can be solved by recursion can be solved by iteration
- Recursion
```java
static int powerOfTwo(int n){
    if(n==0){
        return 1;
    }else{
        int power = 2*powerOfTwo(n-1);
        return power;
    }
}
```
- Iteration
```java
static int powerOfTwo(int n){
    int i=0;
    int power=1;
    while(i<n){
        power=power*2;
        i++;
    }
    return power;
}
```

|Category|Recursion|Iteration|Comments|
|---|---|---|---|
|Space efficient?|No|Yes|No stack memory required in case of iteration|
|Time efficient?|No|Yes|recursion needs more time to push and pop elements to stack memory making it slow|
|Easy to code?|Yes|No|use recursion in case where we know we can divide the problem into sub problems|

### Write recursion in 4 steps
- Step1: Write expected output
- Step2: keep faith that recursive function works for sub problems
- Step3: Connect Step1 and Step2, express expected results using faith
- Step4: Write base conditions and other edge cases

### Fibonacci
- Fibonacci sequence is as 0,1,1,2,3,5,8,13,21,34,55,89
- next number is represented as sum of two previous numbers
- 1st number is 0, second number is 1
```java
public int fib(int n){
    if(n<0){
        return -1;
    }else if(n==0 || n==1){
        return n;
    }else{
        return fib(n-1)+fib(n-2);
    }
}
```