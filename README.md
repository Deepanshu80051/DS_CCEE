# DS_CCEE

# Time and Space Complecxity

Analysis Types (MCQ Important):
Best Case - Minimum time (Omega Ω)
Average Case - Expected time (Theta Θ)
Worst Case - Maximum time (Big-O)

Common Complexities (Fast → Slow):

O(1) - Constant - Array indexing
O(log n) - Logarithmic - Binary search
O(n) - Linear - Linear search
O(n log n) - Linearithmic - Merge sort, Quick sort
O(n²) - Quadratic - Bubble sort, Selection sort
O(2ⁿ) - Exponential - Fibonacci (recursive)
O(n!) - Factorial - Traveling salesman (brute force)


# ADT vs Data Structure (MCQ Important):

ADT - "What" (logical view)
Data Structure - "How" (implementation)
Example:
Stack ADT kehta hai: push(), pop(), peek() operations hone chahiye
Implementation: Array ya Linked List se kar sakte ho

Q: ADT defines:

A) Implementation details
B) Logical operations ✓ (Correct)
C) Memory allocation
D) Programming language

# Array

Initializing array

int [] arr=new int [] {10,20,30,40};  // kar sakte h
int [] arr= {10,20,30,40};  // kar sakte h
int [] arr=new int [4] {10,20,30,40};  // nahi kar kar sakte h

* you cannot mention size and values together
* Java me Object and array - Dyanically bante h - 0
* array is not blank - by default 0
* local - blank
* instance - 1
* eg :- int arr[]
        arr[0] =10;
       arr[1]=30;
       SOP(arr.length)
 // error aaye ga black h na
* eg:- int arr[];
arr =new int [2] 
        arr[0] =10;
       arr[1]=30;
       SOP(arr.length)  //2



# Stack  - LIFO  
Har ek method ka TC-O(i)
Stack Overflow & Underflow:

Overflow - Full stack mein push karne ki koshish
Underflow - Empty stack se pop karne ki koshish

Q: Which application uses Stack?

A) CPU Scheduling
B) Function call management ✓ (Correct)
C) Printer spooling
D) BFS traversal

# Queue - FIFO

Must Remember:

Stack = LIFO, Queue = FIFO
Big-O complexity order: O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2ⁿ) < O(n!)
Circular queue formula: (index + 1) % SIZE
Array indexing: O(1)
All stack/queue basic operations: O(1)









