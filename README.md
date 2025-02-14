# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  
    Probably the most obvious answer is that constants get ignored when
    we are doing asymptotic analysis. There are going to be hidden
    terms added onto the complexity and other constants that get multiplied
    with the time complexity. These do matter for finite values of n.

    Asymptotic analysis looks at the complexity of a function as n
    approaches infinity. However, if n were infinite, it would also
    require infinite memory, which is obviously not realistic. If a program
    uses too much memory, then the program will slow down significantly because
    the computer won't be able to keep up. Therefore, while asymptotic complexity
    describes the behavior as n gets very large, the computer resources might
    cause an algorithm to perform disproportionately worse as n gets large. 

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

    More elements means more memory usage. A computer with not very much memory and tasks
    running in the background could be slowed greatly by using more memory, especially if
    the objects populating the tree also demand a lot of memory. 

    The implementation could also just not be very good. There could be memory leaks for
    whatever reason. The search method could be implemented improperly. Additionally,
    if the tree is filled with more complex objects, it might be slower to compare values
    than it should be.

    It is often necessary to run programs remotely. An unstable connection, low bandwidth or
    excessive activity on the network could greatly impact performance and could cause the
    search to take a lot longer when there are more elements by delaying the flow of data
    from one machine to the other. 

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. 
All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that 
if plagiarism is suspected, charges may be filed against me without prior notice."
