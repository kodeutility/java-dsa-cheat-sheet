# Searching

- Types of searching
    1. Linear search
    2. Binary search

# Time Complexity
|Algorithm|Time Complexity |Space Complexity|
|---|---|---|
|Linear search|O(N)|O(1)|
|Binary search|O(logN)|O(1)|

> For Binary search to work, elements have to be sorted.

# Linear Search
```java
public static int linearSearch(int[] arr, int value){
    for(int i=0;i<arr.length;i++){
        if(arr[i]==value){
            System.out.println("Element is found at index:"+i);
            return i;
        }
    }
    System.out.println("Element not found");
    return -1;
}
```

# Binary Search
- create a function with two parameters which are a sorted array and value
- create two pointers: left pointer and right pointer
- based on left and right pointer calculate mid pointer
- while mid is not equal to the value and start<=end loop:
    - if mid is greater than the value move the right pointer to down
    - if mid is less than value move the left pointer up
- if value to never found return -1

# Recursion Approach
```java
class BinarySearch {
	// Returns index of x if it is present in arr[l..
	// r], else return -1
	int binarySearch(int arr[], int l, int r, int x)
	{
		if (r >= l) {
			int mid = l + (r - l) / 2;

			// If the element is present at the
			// middle itself
			if (arr[mid] == x)
				return mid;

			// If element is smaller than mid, then
			// it can only be present in left subarray
			if (arr[mid] > x)
				return binarySearch(arr, l, mid - 1, x);

			// Else the element can only be present
			// in right subarray
			return binarySearch(arr, mid + 1, r, x);
		}

		// We reach here when element is not present
		// in array
		return -1;
	}

	// Driver method to test above
	public static void main(String args[])
	{
		BinarySearch ob = new BinarySearch();
		int arr[] = { 2, 3, 4, 10, 40 };
		int n = arr.length;
		int x = 10;
		int result = ob.binarySearch(arr, 0, n - 1, x);
		if (result == -1)
			System.out.println("Element not present");
		else
			System.out.println("Element found at index " + result);
	}
}
```

# Iterative Approach
```java
class BinarySearch {
	// Returns index of x if it is present in arr[],
	// else return -1
	int binarySearch(int arr[], int x)
	{
		int l = 0, r = arr.length - 1;
		while (l <= r) {
			int m = l + (r - l) / 2;

			// Check if x is present at mid
			if (arr[m] == x)
				return m;

			// If x greater, ignore left half
			if (arr[m] < x)
				l = m + 1;

			// If x is smaller, ignore right half
			else
				r = m - 1;
		}

		// if we reach here, then element was
		// not present
		return -1;
	}

	// Driver method to test above
	public static void main(String args[])
	{
		BinarySearch ob = new BinarySearch();
		int arr[] = { 2, 3, 4, 10, 40 };
		int n = arr.length;
		int x = 10;
		int result = ob.binarySearch(arr, x);
		if (result == -1)
			System.out.println("Element not present");
		else
			System.out.println("Element found at "+ "index " + result);
	}
}
```

### Note
```java
// This is preferred 
int mid = low + (high – low)/2;
```

```java
// If we calculate middle index like this 
// our code is not 100% correct, it contains bugs.
int mid = (low + high)/2;
```
- It fails for larger values of int variables low and high. Specifically, it fails if the sum of low and high is greater than the maximum positive int value(231 – 1 ).
- The sum overflows to a negative value and the value stays negative when divided by 2. In java, it throws ArrayIndexOutOfBoundException.
- This bug applies equally to merge sort and other divide and conquer algorithms.