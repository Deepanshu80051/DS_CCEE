# DS_CCEE

# Time and Space Complecxity

Analysis Types (MCQ Important):
Best Case - Minimum time (Omega Ω)
Average Case - Expected time (Theta Θ)
Worst Case - Maximum time (Big-O)

Common Complexities (Fast → Slow):

1. O(1) - Constant - Array indexing
2. O(log n) - Logarithmic - Binary search
3. O(n) - Linear - Linear search
4. O(n log n) - Linearithmic - Merge sort, Quick sort4
5. O(n²) - Quadratic - Bubble sort, Selection sort
6. O(2ⁿ) - Exponential - Fibonacci (recursive)
7. (n!) - Factorial - Traveling salesman (brute force)

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

2-D array :- it is array of array

* int arr[][] ; // sahi
* int arr[][]=new int [3][4]; // sahi
*int arr[][]=new int [][];  // error
 * int arr[][]=new int [][4]; // error
 * int arr[][]=new int [3][];  // sahi

 * eg :-
    int arr[][]=new int [3][];
    SOP(arr[0][0]);  // runtime p error
   // nullpointer exception

* eg :-
    int arr[][]=new int [3][];
    SOP(arr[0]);
 o/p- null

* eg :-
     int arr[][]=new int [3][];
    SOP(arr[0].length);
  // null pointer exception

  
# Stack  - LIFO  
Har ek method ka TC-O(1)
Stack Overflow & Underflow:

Overflow - Full stack mein push karne ki koshish
Underflow - Empty stack se pop karne ki koshish

Q: Which application uses Stack?

A) CPU Scheduling
B) Function call management ✓ (Correct)
C) Printer spooling
D) BFS traversal

* :- eg stack
  Traveling bag
  Plate
  Recursion/ fucntioncall

*  Operations :-
    
   Insert - Push()
   Delete - Pop()
   View top element - Peek()
  
*  Ways to implement Stack :-
  Array
  Dynamic Array
  Linked List

  
  ## Polish Notation
The method of wirting operators of an expression either before their operands or after them is called polish notation

1. infix notation  --  A+B
2. Prefix notation -- +AB
3. Postfix noation  -- AB+





# Queue - FIFO

Must Remember:

Stack = LIFO, Queue = FIFO
Big-O complexity order: O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2ⁿ) < O(n!)
Circular queue formula: (index + 1) % SIZE
Array indexing: O(1)
All stack/queue basic operations: O(1)

# Linked List

##difference
1. Memory Allocation:
Array:

Contiguous memory..
Compile-time allocation (static)..
Fixed size..

Linked List:

Non-contiguous (scattered)..
Runtime allocation (dynamic)..
Variable size..
2. Access Time:
Array:

Random access - O(1)..
Direct calculation: base_address + (index × size)..

Linked List:

Sequential access - O(n)..
Traverse karna padta hai..

https://docs.google.com/document/d/17MqAGK9gW4SXz6yUPysh1z1ildN-nxefVbKycbH8wxg/edit?usp=sharing

### Node-based Storage
How Nodes are Stored:

1. **Dynamic Allocation** - `malloc()` ya `new` use karke
2. **Heap Memory** - Nodes heap mein allocate hote hain
3. **Scattered** - Kahi bhi memory mein ho sakte hain
4. **Pointer Connection** - Next pointer se linked

### Memory Management (MCQ Important):

**Array**:
- Stack or static memory
- Contiguous allocation
- Cache-friendly (spatial locality)
- Fixed size at compile time

**Linked List**:
- Heap memory
- Random allocation
- Not cache-friendly
- Dynamic size at runtime

  #### Example Calculation:
```
Singly Linked List with int data:
- Data: 4 bytes
- Pointer: 8 bytes (64-bit)
- Total per node: 12 bytes
100 nodes = 1200 bytes
```
####  Memory Leak:
- Node delete karte time free() karna zaroori
- Nahi toh memory leak hoga
- Pointer lost but memory not freed

Q: Which uses circular linked list?
A: Round-robin CPU scheduling
Q: Singly linked list with 50 nodes (int data, 64-bit system)?
A: 50 × (4 + 8) = 600 bytes

## Recursion
Why Important? (MCQ ke liye yaad rakho):

Termination condition - Recursion rokta hai..
Prevents infinite loop - Stack overflow se bachata hai..
Simplest case - Jo direct solve ho jaye..

* What Happens Without Base Condition?
 ```
 void infiniteRecursion(int n) {
    printf("%d ", n);
    infiniteRecursion(n-1);  // NO BASE CONDITION!
}
// Result: Stack Overflow Error
```

### Key Points (MCQ ke liye):

1. Direct recursion = Function calls itself directly
2. Tail recursion is most optimizable
3. Tree recursion creates exponential calls
4. Linear recursion = single recursive call
5. Head vs Tail depends on call position
6. All these are direct recursion types

### Important Points (MCQ ke liye):

1. **Indirect recursion involves 2+ functions**
2. **Creates circular calling pattern**
3. **Each function needs base condition**
4. **More complex than direct recursion**
5. **Harder to trace and debug**
6. **Stack contains frames from multiple functions**
7. **Used in: State machines, parsers, game AI**

### Common MCQ Pattern:
```
Q: What type of recursion?
void fun1(int n) {
    if(n>0) fun2(n-1);
}
void fun2(int n) {
    if(n>0) fun1(n-1);
}

Answer: Indirect Recursion
```
* Stack frame (Activation record) har function call ke liye create hota hai

## Searching 

1. Linear Search
   * Best Case: O(1) - element pehle position par ho
   * Worst Case: O(n) - element last mein ya exist hi na kare
   * Average Case: O(n)
2. Binary Search
  *  Best Case: O(1) - middle element ho
  * Worst Case: O(log n) - divide and conquer
  * Average Case: O(log n)
  * Kya binary search unsorted array par kaam karega?
   Answer: NO - pehle sort karna padega

## Sorting Algorithms
🫧 Bubble Sort
Concept (Hindi):
Bubble sort mein adjacent elements ko compare karke swap karte hain. Sabse bada element "bubble" ki tarah end tak pahunch jata hai har pass mein..
* Best Case: O(n) - already sorted (with optimization)
* Worst Case: O(n²) - reverse sorted
* Average Case: O(n²)
  
🎯 Selection Sort
Concept (Hindi):
Har iteration mein unsorted portion se minimum element select karo aur usse starting position par swap karo..
* Best, Worst, Average: O(n²) - always same
📥 Insertion Sort
Concept (Hindi):
Cards arrange karne jaisa - ek element uthao aur sorted portion mein sahi jagah insert karo..
* Best Case: O(n) - already sorted
* Worst Case: O(n²) - reverse sorted
* Average Case: O(n²)

  MCQ Pattern:
Kaunsa sort nearly sorted data ke liye best hai?..
Answer: Insertion Sort (O(n) best case)..

🔀 Merge Sort (Divide & Conquer
* Best, Worst, Average: O(n log n) - always consistent
* Space Complexity: O(n)..

 🔀Quick Sort (Divide & Conquer)
 * Best Case: O(n log n) - good pivot selection
* Worst Case: O(n²) - already sorted array (poor pivot)
* Average Case: O(n log n)
* Space Complexity: O(log n) - recursion stack..

🏔️ Heap Sort
* Best, Worst, Average: O(n log n)
* SC O(1)
  
https://docs.google.com/document/d/17MqAGK9gW4SXz6yUPysh1z1ildN-nxefVbKycbH8wxg/edit?usp=sharing

🎓 IMPORTANT MCQ CONCEPTS
1. Stability
Stable: Equal elements ki relative order preserve rahti hai

Stable: Bubble, Insertion, Merge
Unstable: Selection, Quick, Heap

2. In-place vs Not In-place
In-place: Extra space O(1) chahiye

In-place: Bubble, Selection, Insertion, Quick, Heap
Not in-place: Merge (needs O(n))

3. Adaptive
Adaptive: Already sorted data ko fast process kare

Adaptive: Bubble (optimized), Insertion
Non-adaptive: Selection, Merge, Heap, Quick

4. Online
Online: Ek-ek input process kar sake

Online: Insertion
Offline: Baaki sab..

💡 SAMPLE MCQs
Q1: 10 elements ko binary search mein maximum kitne comparisons?

A) 10  B) 4  C) 3  D) 5
Answer: B (log₂10 ≈ 3.32, ceiling = 4)

Q2: Kaunsa sort stable nahi hai?

A) Merge  B) Bubble  C) Quick  D) Insertion
Answer: C (Quick Sort)

Q3: Nearly sorted array ke liye best?

A) Quick  B) Merge  C) Insertion  D) Selection
Answer: C (Insertion Sort - O(n))

Q4: Guaranteed O(n log n) aur stable sort?

A) Quick  B) Heap  C) Merge  D) Selection
Answer: C (Merge Sort)

Q5: 1 million elements, memory tight, fast chahiye?

A) Merge  B) Quick  C) Heap  D) Bubble
Answer: B or C (Quick fast, Heap guaranteed + less space)
