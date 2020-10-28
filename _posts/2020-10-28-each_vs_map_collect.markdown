---
layout: post
title:      "Each vs Map/Collect"
date:       2020-10-28 20:29:33 +0000
permalink:  each_vs_map_collect
---


What's the difference between iterating with each and iterating with map or collect? Both will iterate over the intended elements. The difference lies in the **return**  with these methods.

**Each**

Array.each will take the array and apply the block over each element. However, the original array will be unchanged. In other words, the method will return the original array.

**Map or Collect**

Array.map or Array.collect will take the array, apply the block over each element AND return a changed array (an array with the elements affected by the block). The method will return a *changed* array.

**What does this look like in practice?**

*with each*

             array = [1, 2, 3]

             array.each { |x| puts x + 2}

             *puts out* [3, 4, 5]

             but *returns* [1, 2, 3]


*with map or collect*

             array = [1, 2, 3]

             array.collect { |x| x  + 2}

             *returns* [3, 4, 5]
						
						
So when writing code and requiring a changed array, a programmer can simplify their code by using collect or map to **return a changed array**. 

In the above example, if a programmer wanted to use 'each' but return a changed array affected by the block (increased by 2 (i.e. return an array = [3, 4, 5])), the programmer would need to set a variable equal to an empty array, push each resulting iteration into the new array and then add an additional line that returns the new array. That's 3 additional lines of code that could be replaced by utilizing 'map' or 'collect'!
