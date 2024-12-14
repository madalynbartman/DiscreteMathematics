## Euclid Algorithm: GCD(a,b)
For two non negative integer a, b (a > b), if **r = a mod b** then **GCD(a,b) = GCD(b,r)**

* If we subtract smaller number from larger (we reduce larger number), GCD doesn’t change. So if we keep subtracting repeatedly the larger of two, we end up with GCD.
* Now instead of subtraction, if we divide smaller number, the algorithm stops when we find remainder 0.

### Example
Get GCD(150,165)

GCD(150,165) = GCD(165,150)

= GCD(150,15)    ∵ 165 mod 150 = 15

= GCD(15,0)      ∵ 150 mod 165 = 0

b is zero, therefore complete

GCD(150,165) = 15
## Recursive Algorithm
Recursion in computer science is a method of solving a problem where the solution depends on solutions to smaller instances of the same problem

### Example
when n >= 1, construct a recursive algorithm and get the complexity of f(n)

**f(0) = 1, f(n) = 1 + f(n-1), n >= 1**

f(0) = 1

f(1) = f(0) + 1

f(2) = 1 + f(1) = 1 + [1 + f(0)]

...
```
algorithm sum(int n) {
   s = 0;
   for i = 0 to n
       s = s + 1;
   next i
   return s;
}
```
complexity = O(n)
## Linear Search Algorithm
search an element or value in a given array by traversing the array from the starting, till the desired element or value is found

1. Traverse the array using a for loop.
2. In every iteration, compare the target value with the current value of the array.
  * If the values match, return the current index of the array.
  * If the values do not match, move on to the next array element.
3. If no match is found, return -1.
```
int linearSearch(int values[], int target, int n)
{
    for(int i = 0; i < n; i++)
    {
        if (values[i] == target) 
        {       
            return i; 
        }
    }
    return -1;
}
```
complexity = O(n)
## Binary Search Algorithm
Binary search looks for a particular item by comparing the middle most item of the collection. If a match occurs, then the index of item is returned. If the middle item is greater than the item, then the item is searched in the sub-array to the left of the middle item. Otherwise, the item is searched for in the sub-array to the right of the middle item. This process continues on the sub-array as well until the size of the subarray reduces to zero.
```
Procedure binary_search
   A ← sorted array
   n ← size of array
   x ← value to be searched

   Set lowerBound = 1
   Set upperBound = n 

   while x not found
      if upperBound < lowerBound 
         EXIT: x does not exists.
   
      set midPoint = lowerBound + ( upperBound - lowerBound ) / 2
      
      if A[midPoint] < x
         set lowerBound = midPoint + 1
         
      if A[midPoint] > x
         set upperBound = midPoint - 1 

      if A[midPoint] = x 
         EXIT: x found at location midPoint
   end while
   
end procedure
```
complexity = O(log n)
## Bubble Sort
Bubble Sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in wrong order.
```
begin BubbleSort(list)

   for all elements of list
      if list[i] > list[i+1]
         swap(list[i], list[i+1])
      end if
   end for
   
   return list
   
end BubbleSort
```
complexity = O(n^2)
## Insertion Sort
The array elements are compared with each other sequentially and then arranged simultaneously in some particular order

```
procedure insertionSort( A : array of items )
   int holePosition
   int valueToInsert
	
   for i = 1 to length(A) inclusive do:
	
      /* select value to be inserted */
      valueToInsert = A[i]
      holePosition = i
      
      /*locate hole position for the element to be inserted */
		
      while holePosition > 0 and A[holePosition-1] > valueToInsert do:
         A[holePosition] = A[holePosition-1]
         holePosition = holePosition -1
      end while
		
      /* insert the number at hole position */
      A[holePosition] = valueToInsert
      
   end for
	
end procedure
```
complexity = O(n^2)
## Quick Sort
A large array is partitioned into two arrays one of which holds values smaller than the specified value, say pivot, based on which the partition is made and another array holds values greater than the pivot value.

```
procedure quickSort(left, right)

   if right-left <= 0
      return
   else     
      pivot = A[right]
      partition = partitionFunc(left, right, pivot)
      quickSort(left,partition-1)
      quickSort(partition+1,right)    
   end if		
   
end procedure
```
complexity = O(n^2)
## Merge Sort
Merge sort first divides the array into equal halves and then combines them in a sorted manner.

1. if it is only one element in the list it is already sorted, return.
2. divide the list recursively into two halves until it can no more be divided.
3. merge the smaller lists into new list in sorted order.

```
void merge_sort (int A[ ] , int start , int end ) {
           if( start < end ) {
           int mid = (start + end ) / 2 ;           // defines the current array in 2 parts .
           merge_sort (A, start , mid ) ;                 // sort the 1st part of array .
           merge_sort (A,mid+1 , end ) ;              // sort the 2nd part of array.

         // merge the both parts by comparing elements of both the parts.
          merge(A,start , mid , end );   
} 
```                   
complexity = O(n log n)
