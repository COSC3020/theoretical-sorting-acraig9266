I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice. No sources were used.
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.
# Claim Verification
Since it is a black box implementation I'm allowed to use, there is no way to walk through the algorithm and calculate the time complexity directly. The way I would try to verify the claim would be by feeding the algorithm a large set of randomized inputs that gradually grow in size. With each input, we would track the runtime and create a graph of runtime vs input size. If the graph of the runtime vs size was not linear then this would disprove the claim of the algorithm running in O(n) time complexity.

# Theoretical Argument
Based on the complexity of the general sorting problem from class, the fastest that any general-purpose comparison-based sorting algorithm can be asymptotically is $T(n) ∈ Ω(nlogn)$. Since the researcher is claiming a $O(n)$ for their algorithm, I would say that it could not be correct because he is claiming the fastest growth of his algorithm is slower than the slowest growth of all other general-purpose sorting algorithms and slower growth than the theoretical limit for how fast an algorithm can be.
