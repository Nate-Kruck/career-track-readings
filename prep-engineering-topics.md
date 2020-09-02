# Prep Readings

# Blog Articles Summary

## Quanitity Always Trumps Quality (1)

1. Quantity always trumps quality, so when it comes to perfecting a craft you need to pick a schedule and stick with it. You can't improve on your particular craft until you are mentally committed to doing it over and over.

## Clean Code (2)

### 1. Craftsmanship

- knowledge and work. You must gain
  the knowledge of principles, patterns, practices, and heuristics that a craftsman knows, and
  you must also grind that knowledge into your fingers, eyes, and gut by working hard and
  practicing.

### 2. Learning to Write Code

- Learning to write clean code is hard work. It requires more than just the knowledge of
  principles and patterns. You must sweat over it. You must practice it yourself, and watch
  yourself fail. You must watch others practice it and fail. You must see them stumble and
  retrace their steps. You must see them agonize over decisions and see the price they pay for
  making those decisions the wrong way

### 3. Learning to write clean code

- Writing clean code requires the disciplined use of a myriad little techniques applied
  through a painstakingly acquired sense of “cleanliness.” This “code-sense” is the key.
  Some of us are born with it. Some of us have to fight to acquire it. Not only does it let us
  see whether code is good or bad, but it also shows us the strategy for applying our discipline to transform bad code into clean code

## TDD red-green-factor (3)

### 1. What is TDD?

- Test-driven development (TDD) is an approach to software development where you write tests first, then use those tests to drive the design and development of your software application.

### Red, Green, Refacator

- Red — think about what you want to develop
- Green — think about how to make your tests pass
- Refactor — think about how to improve your existing implementation

### Red

- The red phase is always the starting point of the red, green, refactor cycle. The purpose of this phase is to write a test that informs the implementation of a feature. The test will only pass when the its expectations are met.

- When you run this test, you may see an error message like:

1. sortArray returns an array sorted in ascending order:  
   TypeError: Calculate.arraySort is not a function  
   at Context.it (test/index_test.js:10:32)

As you can see, the purpose of this phase was to define what you want to implement. The resulting error message from this test informs your approach to implementation. At this point, you are considered “in the red.”

### Green

- The green phase is where you implement code to make your test pass. The goal is to find a solution, without worrying about optimizing your implementation.

- At the end of this phase, you are consider “in the green.” You can begin thinking about optimizing your codebase, while having a descriptive test if you do something wrong.

### Refactor

- In the refactor phase, you are still “in the green.” You can begin thinking about how to implement your code better or more efficiently.

## Cycles of TDD (4)

### Second-by-Second nano-cycle: The Three Laws of TDD.

- A few years later this fine granularity was codified into three rules: the so-called Three Laws of TDD.

1. You must write a failing test before you write any production code.
1. You must not write more of a test than is sufficient to fail, or fail to compile.
1. You must not write more production code than is sufficient to make the currently failing test pass.

### Minute-by-Minute: micro-cycle: Red-Green-Refactor

- If we pull back to the minute by minute scale we see the micro-cycle that experienced TDDers follow. The Red/Green/Refactor cycle.

- This cycle is typically executed once for every complete unit test, or once every dozen or so cycles of the three laws. The rules of this cycle are simple.

1. Create a unit tests that fails
1. Write production code that makes that test pass.
1. Clean up the mess you just made.

### Decaminute-by-Decaminute: milli-cycle: Specific/Generic

- At the 10 minute level we see the milli-cycle in operation. The Specific/Generic cycle.

- As the tests get more specific, the code gets more generic.

### Hour-by-Hour: Primary Cycle: Boundaries.

- The final primary cycle of TDD is the cycle that ensures that all the other cycles are driving us towards a Clean Architecture. Ever hour or so we stop and check to see whether we have crossed, or are encroaching upon, a significant architectural boundary.
