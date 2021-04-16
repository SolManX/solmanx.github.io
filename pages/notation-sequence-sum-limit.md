## Notation for sequences, sums and limits

### Basic set notation

A **set** is just a way to collect a number of elements together. For example, the set of all positive integers, called the **natural numbers**, is \\\(\mathbf{N} = \\\{ 1, 2, 3, 4, \ldots \\\} \\\). 

_Note: the ellipsis [\\\( \ldots \\\)] indicates the list continues indefinitely._

Sets can be finite or infinite. In maths, they usually contain numeric values of some kind but more generally they can contain anything. For example, the set of all fruits.

We read 

<p class="indent">\(x \in S\)</p>

as \\\( x \\\) **is an element of**, or, **belongs to**, \\\( S \\\). For example, 

<p class="indent">\( 5 \in \mathbf{N} \)</p>

### Sequence notation

A sequence is just a **set** of values, possibly infinite in length, that can be **indexed** sequentially, i.e. with integers. The most trivial case is the **natural numbers** themselves, the elements of which can be indexed as 

<p class="indent">\(x_1 = 1\), \(x_2 = 2\), \(x_3 = 3\), \(...\).</p>

The general pattern is simply

<p class="indent">\(x_n = n\).</p>

A less trivial case is the even integers, 

<p class="indent">\(x_1 = 2\), \(x_2 = 4\), \(x_3 = 6\), \(...\).</p>

which can be written succinctly as 

<p class="indent">\(\{x_n = 2n: n \in \mathbf{N}\}\).</p>

If we want to emphasize that a particular **set** represents a **sequence**, we often see it written as ...

<p class="indent">\(\{x_n\}_{n \in \mathbf{N}}\)</p>

... but it's usually obvious anyway.

#### Examples
- Odd integers: \\\( \\\{x_n = 2n-1: n \in \mathbf{N} \\\} = \\\{1, 3, 5, 7, \ldots \\\} \\).
- Squares: \\\( \\\{x_n = n^2: n \in \mathbf{N} \\\} = \\\{1, 4, 9, 16, \ldots \\\} \\\).
- Inverses: \\\( \\\{x_n = \frac{1}{n}: n \in \mathbf{N} \\\} = \\\{1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \ldots \\\} \\\).
- Inverse powers of \\\(2 \\\): \\\( \\\{x_n = \frac{1}{2^n}: n \in \mathbf{N} \\\} = \\\{\frac{1}{2}, \frac{1}{4}, \frac{1}{8}, \frac{1}{16} \ldots \\\} \\\).

All of the above examples are of infinite length, but that's not a necessary condition. In the example of the law of large numbers below, we start with a finite sequence of random coin tosses.

### Limits of sequences notation

We want to find out what happens to a **sequence** as we increment it's **index** variable, usually to infinity. The notation for this is either:

<p class="indent">\( L = \lim\limits_{n \to \infty} x_n\)</p>

... or ...

<p class="indent">\(x_n \to L\) as \(n \to \infty\)</p>

Both are read as _the sequence \\\( x_n \\\) tends to the limit, \\\( L \\\), as \\( n \\\) tends to infinity and we are assuming the limit, \\\( L \\\), exists (is not infinite)._

Note that limits do not always exist. For example, there is no limit to the even numbers. We can indicate this using the infinity symbol:

<p class="indent">\(\lim\limits_{n \to \infty} x_n = \infty \)</p>


### Summation notation

Suppose we want to write down the sum, \\\(S\\\), of a well-defined sequence of values. For example, the sum of integers from 1 to 100. We could write this out as:

<p class="indent">\(S = 1 + 2 + 3 + 4 + \ldots + 100\).</p>

The standard notation for this uses the capital of the Greek letter _summa_ and is written:

<p class="indent">\(S = \sum\limits_{k = 1}^{100} k\).</p>

If we want to consider an arbitrary upper index, \\\(n\\\) say, for the sum, we can add a subscript to \\\(S\\\):

<p class="indent">\(S_n = \sum\limits_{k = 1}^{n} k\).</p>


_Note: I'm now using \\\(k\\\) as the index and \\\(n\\\) for the limit below. Anyway it's just a label for indexing._

What about the limit of a sum an of _infinite_ sequence? This is written as:

<p class="indent">\(S = \lim\limits_{n \to \infty} S_n = \lim\limits_{n \to \infty} \sum\limits_{k = 1}^{n} x_k\).</p>

This can be shortened to:

<p class="indent">\(S = \sum\limits_{k = 1}^{\infty} x_k\).</p>

Note it is possible to have a finite result of an infinite sum. For example, the sum of the inverse powers of \\\(2\\\) add up to \\\(1\\\):

<p class="indent">\(\sum\limits_{k = 1}^{\infty} \frac{1}{2^k} = \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \frac{1}{16} + \ldots = 1\).</p>

#### Example: Law of large numbers

Suppose we have a sequence of random coin tosses, \\\(X\\\), which we could write as:

<p class="indent">\(X = \{0, 1, 1, 1, 0, 0, 1, \ldots\, 1, 0\}\).</p>

Or, more generally:

<p class="indent">\(X = \{x_k \in \{0, 1\}: k \le 100\} \).</p>

_It's assumed that the coin is fair, so the probabilities of heads (\\\(1\\\)) and tails (\\\(0\\\)) are both 50%._


We could make it even more general by indicating an arbitrary number of coin tosses, \\\(n\\\) say:

<p class="indent">\(X_n = \{x_k \in \{0, 1\}: k \le n\} \)</p>

Here,

- \\\(X_n\\\) is the sequence of all the coin tosses
- \\\(k\\\) is the index of the coin toss
- \\\(x_k\\\) is the value of the coin toss (i.e. either (\\\(1\\\) or \\\(0\\\))
- \\\(n\\\) is the number of coin tosses

To calculate the **expected value, \\\(E\\\)** of the sum of the sequence \\\(X_n\\\), we need to take the average. That is, we sum up the \\\(1\\\)'s and \\\(0\\\)'s and then divide the whole thing by the number of tosses:

<p class="indent">\( E(X_n) = \frac{1}{n} \sum\limits_{k = 1}^{n} x_k \).</p>

Finally (phew!), we can ask what happens to this value as we make \\\(n\\\) larger and larger. In fact we can ask if the limit exists as \\\(n\\\) tends to infinity. And we know what this expected value is, namely \\\( \frac{1}{2}\\\). That is,

<p class="indent">\( E = \lim\limits_{n \to \infty} E(X_n) = \lim\limits_{n \to \infty} \frac{1}{n} \sum\limits_{k = 1}^{n} x_k = \frac{1}{2}\).</p>
