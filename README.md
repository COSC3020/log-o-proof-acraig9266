# Need to change to base 2 and base 5

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
This means that 1.5849618816667(nlog(base3)(n)) is equivalent to writing nlog(base2)(n). Since the c value in big O is a constant that simply has to be greater than 0, we can multiply the c that satisifies big O for nlog(base2)(n) by 1.5849618816667 and the new value of c would then satisfy big O for nlog(base3)(n)). Since we can always multiply or divide c by a known factor to account for switching between different bases, the base of the log used in the big O can be left off since C can just be adjusted.

The link below is for a desmos graph that demonstrates visually that 2.32192809(log(base5)(x)) = log(base2)(x)
https://www.desmos.com/calculator/wzu5ibiylr
