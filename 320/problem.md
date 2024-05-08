## Description

<div><p>Pak Chanek loves his faculty, the Faculty of Computer Science, University of Indonesia (Fasilkom). He wants to play with the colours of the faculty's logo, blue and red.</p><p>There is an array $a$ consisting of $n$ elements, element $i$ has a value of $a_i$. Pak Chanek wants to colour each element in the array blue or red such that these following conditions are satisfied: </p><ul> <li> If all blue elements are formed into a subsequence$^\dagger$ and so are all the red elements, the blue subsequence is strictly less than the red subsequence lexicographically$^\ddagger$. </li><li> Array $a$ does not have <span class="tex-font-style-bf">any subarray</span> that is imbalanced. A subarray is imbalanced if and only if there is a value $k$ such that the absolute difference between the number of blue elements with value $k$ and the number of red elements with value $k$ in this subarray is $2$ or more. </li><li> Note that it is possible to colour every element of the array the same colour. </li></ul><p>How many different colourings satisfy all those conditions? Since the answer can be very big, print the answer modulo $998\,244\,353$. Two colourings are different if and only if there is at least one element that is blue in one colouring, but red in the other.</p><p>$^\dagger$ A subsequence of an array is a sequence that can be obtained from the array by deleting some elements (possibly none), without changing the order of the remaining elements.</p><p>$^\ddagger$ Let $p$ and $q$ be two different sequences. Sequence $p$ is said to be lexicographically less than sequence $q$ if and only if $p$ is a prefix of $q$ or there is an index $i$ such that $p_j=q_j$ holds for every $1\leq j&lt;i$, and $p_i&lt;q_i$. In particular, an empty sequence is always lexicographically less than any non-empty sequence.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \leq n \leq 2\cdot10^5$) — the size of array $a$.</p><p>The second line contains $n$ integers $a_1,a_2,a_3,\ldots,a_n$ ($1\leq a_i\leq2\cdot10^5$).</p></div><div class="output-specification"><p>An integer representing the number of different colourings that satisfy all of the problem's conditions, modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \leq n \leq 2\cdot10^5$) — the size of array $a$.</p><p>The second line contains $n$ integers $a_1,a_2,a_3,\ldots,a_n$ ($1\leq a_i\leq2\cdot10^5$).</p>

## Output

<p>An integer representing the number of different colourings that satisfy all of the problem's conditions, modulo $998\,244\,353$.</p>





```input1
8
1 3 1 2 3 2 3 3
```




```input2
1
265
```




```output1
3
```




```output2
1
```



## Note

<p>In the first example, the $3$ ways for colouring all elements from index $1$ to index $8$ are: </p><ul> <li> <span class="tex-font-style-bf">Blue, red, red, blue, blue, red, red, blue</span>. </li><li> <span class="tex-font-style-bf">Blue, red, red, red, blue, blue, red, blue</span>. </li><li> <span class="tex-font-style-bf">Red, red, blue, blue, blue, red, red, blue</span>. </li></ul><p>As an example, if we colour the elements from index $1$ to index $8$ to be <span class="tex-font-style-bf">red, red, blue, red, red, blue, blue, blue</span>, it is not valid colouring, because for subarray $a[2..6]$, there are $0$ blue elements with value $3$ and $2$ red elements with value $3$, making subarray $a[2..6]$ an imbalanced subarray.</p>
