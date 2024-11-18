# Plagiarism Acknowledgement
I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
The only source used was Desmos to explore the relation between logs of different bases by graphing them. Link to graph: https://www.desmos.com/calculator/pyarjzuudf

# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

Any two logarithms of different bases always differ by a constant factor when given the same value for the argument.
For example, a log(base 2)(x) is always a constant factor of approximately (find new factor) times log(base 5)(X) for x > 1
This means that 2.32192809(nlog(base3)(n)) is equivalent to writing nlog(base2)(n). Since the c value in big O is a constant that simply has to be greater than 0, we can multiply the c that satisifies big O for nlog(base2)(n) by 2.32192809 and the new value of c would then satisfy big O for nlog(base5)(n)). Since we can always multiply or divide c by a known factor to account for switching between different bases, the base of the log used in the big O can be left off since C can just be adjusted with the log base.

