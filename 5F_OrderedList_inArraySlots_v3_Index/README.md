# implement List.indexOf

`while`-style and recursive implementations at the top of
OrderedList_inArraySlots.java

[Java API on the `indexOf` method](https://docs.oracle.com/javase/10/docs/api/java/util/List.html#indexOf(java.lang.Object))

based on [solutionsHolmes/5D_genericTypes/OrderedList_inArraySlots_v2/](https://github.com/stuyvesant-cs/solutionsHolmes/tree/master/5D_genericTypes/OrderedList_inArraySlots_v2)
as of 2019-04-10 04:48

What is meant by y = log2x? What does its graph look like?
2 raised to the y power equals x. The log graph is only in Quadrant I and Quadrant IV and the increase rate of y decreases as x increases.

State the problem
Find the location of an element in a list of size n.

State the recursive abstraction
When asked to find the location of an element in a list of size n, 
the recursive abstraction is able to find the location of an element in a list of size n/2.

Identify the parts of this solution that correspond to the six parts of a generalized recursive solution.
Decisions
 -if( low > hi)
 -if( comparison == 0)
 
Solutions to base cases
 -return -2;
 -return pageToCheck;
Solution to recursive cases
 -leftover processing
 -combining element 
 -recursive abstraction
  -return indexOf_recursive( findMe, low, pageToCheck -1);
  -return indexOf_recursive( findMe, pageToCheck +1, hi);