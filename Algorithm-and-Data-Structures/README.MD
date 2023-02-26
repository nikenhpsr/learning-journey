# Algorithm & Data Structures

## Section

- [Algorithm](#algorithm)
- [Algorithm Design](/Algorithm-and-Data-Structures/algorithm-design.md)
- [Algorithm Part](/Algorithm-and-Data-Structures/algorithm-design.md)
- [Algorithm Building Blocks](/Algorithm-and-Data-Structures/algorithm-design.md)
- [Data Structures](/Algorithm-and-Data-Structures/DSA.md)

## **Algorithm**

Algorithm is a way to develop a step by step solution to the problem or the rules to follow to solve the problem. Most of the time we have to use our own or our collective logic to build an algorithm. Algorithm mostly consists of:
- Input : Data and their quantities
- Process : Steps, Functions or Methods
- Output : Finished result

Algorithms are normally written using one of the following conventions:
- Pseudo-code
- Flowcharts
- Written descriptions
- Program code

### **Pseudo-code**

Pseudo-code is not a programming language. Instead, it is a simple way of describing a set of programming instructions in a manner that resembles a programming language. This simple pseudo-code algorithm asks a user to input what their favourite subject is:

```
WHILE answer <> 'computer science' DO
                         SEND 'What is your favourite subject?' TO 
                         DISPLAY
                         RECEIVE answer FROM (STRING) KEYBOARD
                         IF answer = 'computer science' THEN
                              SEND 'Good choice!' TO DISPLAY
                         ELSE
                              SEND 'Really? ' TO DISPLAY
                         END IF
                    END WHILE
```

### **Flowchart**

A flowchart is a diagram that shows an overview of a program. Flowcharts normally use standard symbols to represent the different types of instructions. These symbols are used to construct the flowchart and show the step-by-step solution to the problem.

**[You can see the flowchart symbols in here](https://www.zenflowchart.com/flowchart-symbols)**

### **Written Description**

There is no defined format for this, so programmers are free to write as they wish. Short sentences are best. An algorithm should be easy to understand and have no unnecessary detail. A recipe is a good example of clear instructions, eg ‘stir’ and ‘bake’.

### **Program Code**

Program code can also be used to create an algorithm. In this context it is called draft program code. There is no requirement for an algorithm to compile and run so errors are acceptable so long as the meaning is clear.

## **Standard Algorithms**

Two types of algorithm that are often used are searches and sorts. Searches enable a data set to be examined and a specific item to be found. Sorts enable a data set to be sorted into order.

Standard searching algorithms include:

### **1. Linear Search**

A linear search is the simplest method of searching a data set.

Starting at the beginning of the data set, each item of data is examined until a match is made. Once the item is found, the search ends. If there is no match, the algorithm must deal with this.

A written description algorithm for a linear search might be:

1. Find out the length of the data set.
2. Set counter to 0.
3. Examine value held in the list at the counter position.
4. Check to see if the value at that position matches the value searched for.
5. If it matches, the value is found. Send a message and end the search.
6. If not, increment the counter by 1 and go back to step 3 until there are no more items to search.
7. If all the items have been checked and no match is found, send a message.

Although simple, a linear search can be quite inefficient. Suppose the data set contained 100 items of data, and the item searched for happens to be the last item in the set. All of the previous 99 items would have to be searched through first.

However, linear searches have the advantage that they will work on any data set, whether it is ordered or unordered.

### **2. Binary Search**

A binary search is an efficient method of searching an ordered list. It will not work on a list that has not been sorted first.

A written description of a binary search algorithm is:

1. Start by setting the counter to the middle position in the list.
2. If the value held there is a match, the search ends and a message is sent.
3. If the value at the midpoint is less than the value to be found, the list is divided in half, the lower half of the list is ignored and the search keeps to the upper half of the list.
4. Otherwise, if the value at the midpoint is greater than the value to be found, the upper half of the list is ignored and the search keeps to the lower half of the list.
5. The search moves to the midpoint of the remaining items. Steps two to four continue until a match is made or there are no more items to be found and a message is sent.

A binary search is a much more efficient algorithm than a linear search. In an ordered list of every number from 0 to 100, a linear search would take 99 steps to find the value 99. A binary search would only require 7 steps.

However, a binary search can only work if a list has been sorted into order.
Standard sorting algorithms include:

### **1. Bubble Sort**

A bubble sort is the simplest of the sorting algorithms. However, it is an inefficient sort for anything but a small list because of the number of comparisons required.

A written description algorithm of a bubble sort is:

1. Start at the beginning of the list.
2. Compare the first value in the list with the next one up. If the first value is bigger, swap the positions of the two values.
3. Move to the second value in the list. Again, compare this value with the next and swap if the value is bigger.
4. Keep going until the there are no more items to compare. Note - the last item checked in the list is now sorted, so ignore this next time.
5. Go back to the start of the list.

Each run through the list, from start to finish, is known as a pass. The bubble sort continues until a pass is made where no values have been swapped. At this point, the list is sorted.

### **2. Merge Sort**

A merge sort is a more complex sort, but also a highly efficient one.

A merge sort uses a technique called divide and conquer. The list is repeatedly divided into two until all the elements are separated individually. Pairs of elements are then compared, placed into order and combined. The process is then repeated until the list is recompiled as a whole.

## **Computational Thinking**

Computers can be used to help solve problems. However, before a problem can be tackled, the problem itself - and the ways in which it could be solved - needs to be understood.

Computational thinking helps with this. It allows us to take a complex problem, understand what the problem is and develop possible solutions. These solutions can then be presented in a way that a computer, a human, or both can understand.

### **Complex problems and computational thinking**

A complex problem is one that - at first glance - does not have an obvious, immediate solution.

Computational thinking involves taking that complex problem and breaking it down into a series of small, more manageable problems.

Each of these smaller problems can then be looked at individually.

Next, simple steps to solve each of the smaller problems can be designed.

Finally, these simple steps are used to program a computer to help solve the complex problem in the best way.

### **Logical reasoning**

Logical reasoning is not programming. Put simply, programming tells a computer what to do and how to do it. Logical reasoning enables programmers to work out exactly what to tell the computer to do.

For example, if you agree to meet your friends somewhere you have never been before, you would probably plan your route before you step out of your house. You might consider the routes available and which route is ‘best’. This might be the route that is the shortest, the quickest, or the one which goes past your favourite shop on the way. You'd then follow the step-by-step directions to get there.

In this case, the planning part is logical reasoning, and following the directions is like programming.

Being able to turn a complex problem into one that can be easily understood is a skill that is extremely useful.

Two important elements of computational thinking are:

### **1. Decomposition**

Decomposition involves analysing a complex problem or system and breaking it down into smaller parts that are more manageable and easy to understand. The smaller parts can then be examined and solved, or designed individually, as they are simpler to work with.

If a problem is not decomposed, it is much harder to solve. Dealing with a complex problem is much more difficult than breaking a problem down into subproblems and solving them, one at a time. Smaller problems are easier to understand and can be examined in more detail.

### **2. Abstraction**

Abstraction is the process of filtering out - essentially ignoring - the characteristics of problems that are not needed in order to concentrate on those that are needed. It is also the filtering out of specific details. From this, an idea of what is to be solved can be created.

Abstraction allows programmers to create a general idea of what the problem is and how to solve it. The process instructs them to remove all specific detail and any patterns that will not help find a solution. An idea of the problem can then be formed. This idea is known as a ‘model’.

## Resources

- [Algorithms](https://www.notion.so/Algorithm-9b8ff5ffc38b43b5a6d2f2e975ca2dd7) - Catamyst
- [What is an Algorithms?](https://www.bbc.co.uk/bitesize/guides/z22wwmn/revision/1) - GCSE Computer Science
