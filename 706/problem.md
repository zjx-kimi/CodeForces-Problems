## Description

<div><p>Mihai and Bianca are playing with bags of candies. They have a row $a$ of $n$ bags of candies. The $i$-th bag has $a_i$ candies. The bags are given to the players in the order from the first bag to the $n$-th bag. </p><p>If a bag has an even number of candies, Mihai grabs the bag. Otherwise, Bianca grabs the bag. Once a bag is grabbed, the number of candies in it gets added to the total number of candies of the player that took it. </p><p>Mihai wants to show off, so he wants to reorder the array so that at any moment (except at the start when they both have no candies), Mihai will have <span class="tex-font-style-bf">strictly more</span> candies than Bianca. Help Mihai find out if such a reordering exists.</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 100$)&nbsp;— the number of bags in the array.</p><p>The second line of each test case contains $n$ space-separated integers $a_i$ ($1 \leq a_i \leq 100$)&nbsp;— the number of candies in each bag.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if such a reordering exists, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 100$)&nbsp;— the number of bags in the array.</p><p>The second line of each test case contains $n$ space-separated integers $a_i$ ($1 \leq a_i \leq 100$)&nbsp;— the number of candies in each bag.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes) if such a reordering exists, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,6,7
3
4
1 2 3 4
4
1 1 1 2
3
1 4 3
```




```output1
YES
NO
NO
```



## Note

<p>In the first test case, Mihai can reorder the array as follows: $[4, 1, 2, 3]$. Then the process proceeds as follows: </p><ul> <li> the first bag has $4$ candies, which is even, so Mihai takes it&nbsp;— Mihai has $4$ candies, and Bianca has $0$. </li><li> the second bag has $1$ candies, which is odd, so Bianca takes it&nbsp;— Mihai has $4$ candies, and Bianca has $1$. </li><li> the third bag has $2$ candies, which is even, so Mihai takes it&nbsp;— Mihai has $6$ candies, and Bianca has $1$. </li><li> the fourth bag has $3$ candies, which is odd, so Bianca takes it&nbsp;— Mihai has $6$ candies, and Bianca has $4$. </li></ul> Since Mihai always has more candies than Bianca, this reordering works.
