## Asymptotic Notations

##### What are Asymptotic Notations?

Think of asymptotic notations as a set of tools in the world of computer science and mathematics that help us describe how the performance or efficiency of algorithms and functions behaves as their input size grows larger and larger. It's like having a language to talk about how well our code performs in the long run.

###### Why are Asymptotic Notations Important?

Picture this: You're a chef, and you need to make a recipe for a large group of people. You want to know how much time and effort it will take to cook for 10, 100, or 1000 guests. Similarly, in computer science, we use asymptotic notations (like Big O, Omega, and Theta) to predict how our algorithms will perform when we deal with a small dataset, a medium-sized one, or a colossal one.

Asymptotic notations help us understand and compare the efficiency of different algorithms without getting bogged down in the nitty-gritty details of specific hardware or programming languages. They provide a high-level view of how well our code scales, allowing us to choose the best algorithm for a given problem and optimize our software for real-world applications.

##### Some important guidelines:

When it comes to comparing algorithms and their efficiency using asymptotic notations, it's essential to follow some straightforward guidelines to make the process more manageable. Here are two key strategies:

1. **Ignore Lower-Order Terms:**
   
   In the world of asymptotic analysis, not all terms in a mathematical expression are created equal. When comparing algorithms, it's often unnecessary to consider every term. Lower-order terms are those with lower degrees or exponents, and they become less significant as the input size grows.
   
   Imagine you have two algorithms, Algorithm A and Algorithm B. The time complexities for Algorithm A and B are represented as follows:
   
   - Algorithm A: O(n^2 + 3n + 5)
   - Algorithm B: O(4n^3 + 2n^2 + 7n + 1)
   
   In this case, when comparing these algorithms, you can safely ignore the constants (3, 5, 4, 2, 7, and 1) and the lower-order terms (n and n^2). This simplifies the comparison to:
   
   - Algorithm A: O(n^2)
   - Algorithm B: O(n^3)
   
   By focusing on the higher-order terms (n^2 and n^3), you can easily determine that Algorithm B has a worse time complexity than Algorithm A as the input size grows.

2. **Ignore Leading Term Constants:**
   
   The leading term in an algorithm's time complexity expression is the one with the highest degree or exponent. It dominates the behavior of the algorithm as the input size becomes large. To simplify algorithm comparisons, you can disregard the constant factors in front of the leading term.
   
   Let's consider another example with Algorithm C and Algorithm D:
   
   - Algorithm C: O(5n^2)
   - Algorithm D: O(0.5n^2)
   
   Although Algorithm C appears to have a larger constant (5), it's not relevant when comparing their asymptotic growth. When you remove the leading term constants, the comparison becomes:
   
   - Algorithm C: O(n^2)
   - Algorithm D: O(n^2)
   
   In this case, both algorithms have the same growth rate, indicating similar efficiency.



##### Complexity comparison:

Here is a general guideline

![](data:image/png;base64,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)



##### Common Tools:

**Big O Notation (O):**

Big O notation, often denoted as O(f(n)), provides an upper bound on the growth rate of an algorithm's time complexity as the input size (n) increases. It represents the worst-case scenario, indicating that the algorithm will not perform worse than this bound. In simpler terms, it describes the maximum time an algorithm will take to complete its task.

For example, if we say an algorithm has a time complexity of O(n^2), it means that the algorithm's execution time grows no faster than n^2 as the input size increases. This is useful when you want to understand the worst-case efficiency of an algorithm.

**Omega Notation (Ω):**

Omega notation, denoted as Ω(f(n)), provides a lower bound on the growth rate of an algorithm's time complexity. It represents the best-case scenario, indicating that the algorithm will not perform better than this bound. In other words, it describes the minimum time an algorithm will take to complete its task.

For instance, if we say an algorithm has a time complexity of Ω(n), it means that the algorithm's execution time will be at least proportional to n as the input size increases. Omega notation helps us understand the best-case efficiency of an algorithm.

**Theta Notation (Θ):**

Theta notation, represented as Θ(f(n)), provides a tight bound on the growth rate of an algorithm's time complexity. It defines both an upper and a lower bound that are essentially the same. In simpler terms, it describes the precise growth rate of an algorithm, and it's often used to describe the average-case behavior.

For example, if we say an algorithm has a time complexity of Θ(n), it means that the algorithm's execution time will grow exactly proportionally to n as the input size increases. Theta notation is valuable when you want to analyze an algorithm's performance under typical conditions.



##### **Space Complexity:**

Space complexity is a measure of the amount of memory or storage space required by an algorithm to execute as a function of the input size (n). In other words, it quantifies how efficiently an algorithm utilizes memory as it processes data. Space complexity is crucial because it helps us understand the memory requirements of an algorithm, which is essential for efficient resource management in computer systems.

When analyzing space complexity, we typically consider the following:

- **Input Space:** The space required to store the input data or any auxiliary data structures needed for computation.
- **Output Space:** The space required to store the output data or any intermediate results.
- **Fixed Overhead:** The space consumed by fixed-size variables, constants, and code instructions.
- **Dynamic Space:** The space used by dynamically allocated data structures like arrays, lists, trees, or stacks during algorithm execution.

Space complexity is often expressed using Big O notation (e.g., O(f(n))), similar to time complexity. It provides insights into how the memory usage grows with increasing input size. For example, if an algorithm has a space complexity of O(n), it means the memory usage increases linearly with the input size.



**Auxiliary Space (Extra Space):**

Auxiliary space, also referred to as extra space, is a specific aspect of space complexity. It represents the additional memory space an algorithm needs beyond the space required for input data and the algorithm's variables. In essence, it quantifies the memory overhead introduced by an algorithm during its execution.

Auxiliary space excludes the space used for the input, output, and other fixed overhead, focusing solely on the extra memory required for temporary storage and bookkeeping. It helps us understand how an algorithm's memory usage is affected by auxiliary data structures, recursion, or other memory-intensive operations.

For example, consider a sorting algorithm like merge sort. It requires additional space to create temporary arrays during its execution. The space complexity might be O(n) in terms of auxiliary space because it uses extra memory proportional to the input size to perform the sorting.
