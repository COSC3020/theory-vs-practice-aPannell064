# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
    Probably the most obvious answer is that constants get ignored when
    we are doing asymptotic analysis. There are going to be hidden
    terms added onto the complexity and other constants that get multiplied
    with the time complexity. These do matter for finite values of n.

    Computers usually have many different programs operating in the background.
    If too much memory is being used, either through background tasks or the program
    tbat is being run, then there will be some significant slow downs and the computer
    won't be able to keep up. Asymptotic analysis is more focused on perfect conditions,
    but it doesn't take hardware limitations into account. 

    You can write the same program in different languages with the same complexity,
    but changing the language or the compiler could make a program perform mysteriously
    faster or slower, even if the number of steps remain the exact same. There could
    be unexpected differences at a lower level. As a result, two programs that do the
    same thing, but in different languages could perform very differently. 

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

    More elements means more memory usage. If most of a computer's memory is already being
    used, it might not have enough to quickly proccess ten times as many elements. While this
    wouldn't likely be a porblem if integers are being compared, real world applications often
    require much more complex objects. Comparisons of large objects could quickly use up system
    memory and reduce the performance of the search. 

    The implementation could also just not be very good. There could be memory leaks for
    whatever reason. The search method could be implemented improperly. Comparisons of complex
    objects, might take way more time and memory than they should. These would all reduce performance. 

    Many computers have systems that throttle the processor if the computer has to work harder. The
    increase in the amount of elements, especially if they are complex, could potentially lead to
    issues like thermal throttling, which would not be reflected by asymptotic analysis. 

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. 
All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that 
if plagiarism is suspected, charges may be filed against me without prior notice."
