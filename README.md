# Pancake Sort

There is an abstract data type (ADT) called a *pancake array*, which provides
the function `flip(array, n)`, which takes the top (first) $n$ items in the
array and "flips them over", i.e. reverses their order.

For example, if you called `flip([1, 2, 3, 4], 2)`, the result would
be the array  `[2, 1, 3, 4]`, because the order of the (first) top 2
elements in the array has been reversed.

If $n$ is larger than the number of items in the array, the entire array gets
reversed. The intuition for the name "pancake array" is that with a stack of
pancakes, you can insert a spatula at any point in the stack and use it to flip
over all pancakes above that point.

Implement a sorting function that will sort an array of pancakes such that the
smallest pancake is at the top. You may use only the `flip()` function to
manipulate the array. You may break ties arbitrarily. Test your new function;
I've provided some basic testing code that uses
[jsverify](https://jsverify.github.io/) in `code.test.js`, but it only tests
`pancakeSort()`, not `flip()`.

Hint: Start by thinking about the calls to `flip()` required to move a *single*
element into its correct position.

## Runtime Analysis

What is the asymptotic runtime ($\Theta$) of your algorithm in terms of the
number of comparisons of pancakes? What is it in terms of the number of flips?
Add your answer to this markdown file.

The average asymptotic runtime would be $\Theta(n^2)$, this is because in our main pancake sort function when we find the max value in the part of the array we are looking at this runtime would be $n^2$. Then, if the max value is not already in the front of the array to flip to the other end, we can call the flip function twice, which has a for loop reversing the order and would be $2n$. For the number of flips, like said before, if the max value is in the front at the 0 element position then we call flip once resulting in $n$. If the max value is not in the front, we call flip twice resulting in $2n$.


Citations: I worked with Olivia, Ashlyn, and Cole(Nathanial). I also went to the TA's office hours and found my flip function's logic was incorrect, so I fixed it later and further realized after fixing flip I had a couple things to fix in my pancake sort when running the tests. 

I subimtted this work Fall 2024.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

