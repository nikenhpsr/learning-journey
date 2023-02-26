# Algorithms Design

When designing an algorithm, consider if there is more than one way of solving the problem.

When designing an algorithm there are two main areas to look at:

- **The big picture** - What is the final goal?
- **The individual stages** – What hurdles need to be overcome on the way to the goal?

## Understanding the problem
Before an algorithm can be designed, it is important to check that the problem is completely understood. There are a number of basic things to know in order to really understand the problem:

- What are the inputs into the problem?
- What will be the outputs of the problem?
- In what order do instructions need to be carried out?
- What decisions need to be made in the problem?
- Are any areas of the problem repeated?

Once these basic things are understood, it is time to design the algorithm.

## Algorithm Design Examples

- **Searching**: Searching for data can be very difficult. Searching algorithms, such as serial search and binary search, make the process of searching for data much easier. Search algorithms prevent you from having to look through lots of data to find the information you are searching for.
    - serial search
    - binary search
- **Sorting**: Putting data into order can be difficult and time-consuming. Sorting algorithms, such as bubble sort and bucket sort can help with this.
    - bubble sort
    - bucket sort



# Algorithm Parts

Algorithms have data values that can be constant (fixed) or variable. These values are stored in a memory location and can be changed, depending on the output that is needed.

## Constants

Data values that stay the same every time a program is executed are known as constants. Constants are not expected to change.

Literal constants are actual values fixed into the source code. An example of this might be the character string "hello world". The data value "hello world" has been fixed into the code.

Named constants are values where a name is defined to be used instead of a literal constant. An example of this might be stating that the 'starting level' of a game is always referred to as 1.

Examples of a constant within a game might be:

- the unit of gravity
- the number of lives available for the player
- the amount of time allowed for a level in a game

## Variables

Variables are data values that can change when the user is asked a question, for example, their age. Variables may change during program execution.

A variable is a memory location. It has a name that is associated with that location. The memory location is used to hold data.

## Assignment

In order to change the data value stored in a variable, you use an operation called assignment. This causes the value to be copied into a memory location, overwriting what was in there before.

Different values may be assigned to a variable at different times during the execution of a program. Each assignment overwrites the current value with a new one.

## Scope

The scope of variables can be local or global.

- **local** variables only work in the loop, procedure or class they are created in
- **global** variables can be accessed from any point in a program

## Declarations

Declaring a name for a variable is saying what the data type will be and where it will be stored in memory.


# Algorithm Building Blocks (Constructs)

## Sequencing

Sequencing is the specific order in which instructions are performed in an algorithm. Algorithms consist of instructions that are carried out (performed) one after another. It is crucial that the steps in an algorithm are performed in the right order. Otherwise, the algorithm will not work correctly. A computer can only do what it is programmed to do. If the steps are programmed in the wrong sequence, the computer will perform the tasks in this sequence – even if this is incorrect.

Sequencing is implemented in programming using:

- `NAME`/`KEY` variable
- `PRINT` or `LOG` statement
- `=` assignment expression
- `+`, `-`, `*`, `/`, `%`, and other operator expression

## Selection

Selection is a decision or question. The selection allows there to be more than one path through a program. At some point, a program may need to ask a question because it has reached a step where one or more options are available. Depending on the answer given, the program will follow a certain step and ignore the others.

Selection is implemented in programming using:

- `IF` statement
- `IF...ELSE` statement
- `ELSE IF` statement

## Iteration

Iteration is the process of repeating steps. Algorithms consist of steps that are carried out (performed) one after another. Sometimes an algorithm needs to repeat certain steps until told to stop or until a particular condition has been met. Iteration allows us to simplify our algorithm by stating that we will repeat certain steps until told otherwise. This makes designing algorithms quicker and simpler because they don’t have to include lots of unnecessary steps.

There are two ways in which programs can iterate or 'loop':

- **count-controlled** loops: in a range of numbers, such as from 0 to 100
- **condition-controlled** loops: in a specific condition, such as when the toggle is true

Iteration is implemented in programming using:

- `FOR` statement
    - `FOR...OF` statement
    - `FOR...IN` statement
- `WHILE` statement
    - `DO WHILE` statement

## Logical Reasoning

Logical reasoning is the process of applying rules to problem-solving. Algorithms are designed as a set of steps to follow to solve a problem. At the same time, a set of rules is determined.

Rules are built using logical reasoning to ensure that the algorithm performs correctly.

When trying to solve a problem, it may be that more than one solution is found. A different algorithm can be built from each solution. Logical reasoning determines if algorithms will work by predicting what happens when the algorithm’s steps (and the rules they consist of) are followed.

Predictions from each algorithm can be used to compare solutions and decide on the best one.