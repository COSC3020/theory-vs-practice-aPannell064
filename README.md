# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
      Probably most obvious answer is that constants get ignored when
      we are doing asymptotic analysis. There are going to be hidden
      term added onto the complexity and other constants that get multiplied
      with the time complexity. These do matter for finite values of n.

      If a program is very intensive, it could end up using many more resources
      than it should for large n values. In extreme cases this could potentially
      slow down the program significantly, even if it is asymptotically fast.

      It's usually a good idea to program to make the common case fast. However,
      when you may expect the common case to be the average case, this might not
      be true. If the worst case is the common case, a program that is a little
      slower with the average and best case, but stays consistent with the worst case
      might perform better more often in practice than a program more geared towards the
      average case. 

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

      Finding a element in a binary search tree is expressed with a complexity of
      $\Theta(log(n))$. While the logarithmic base doesn't usually matter in asymptotic
      complexity we know that it's in base 2 because of how a binary search tree works.
      $log_2(1000) \approx 9.97$ indicating that it takes about half a second for each level
      on the tree. $log_2(10000) \approx 13.29$. Therefore, it would probably take about
      6.5 to 7 seconds to find the same element in a larger tree. However, this doesn't
      consider where the actual element is in each of the trees. If the element is the
      same depth in, it should take about the same amount of time regardless of the number
      of elements. Additionally, if it's shallow in the 1,000 element tree, but deep in the
      10,000 element tree it could take significantly longer. 

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

      If the data is sorted or almost sorted, the tree becomes about as useful as a linked
      list, which would probably make it take significantly longer. It would be better to use
      AVL or Red/Black trees in this case.  

      The implementation could also just not be very good. There could be memory leaks for
      whatever reason. The search method could be implemented improperly. Additionally,
      if the tree is filled with more complex objects, it might be slower to compare values
      than it should be.

      Constants and additional terms that were ignored in the asymptotic complexity could become
      more relevant in a finite data set. These constants might have especially been overlooked if
      the element was shallow in the 1,000 element tree, but deep in the 10,000 element tree.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. 
All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that 
if plagiarism is suspected, charges may be filed against me without prior notice."
