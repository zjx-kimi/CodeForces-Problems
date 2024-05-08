## Description

<div><p><span class="tex-font-style-it">This is the easy version of the problem. The only difference is that in this version everyone must give candies to <span class="tex-font-style-bf">exactly one</span> person and receive candies from <span class="tex-font-style-bf">exactly one</span> person. Note that a submission cannot pass both versions of the problem at the same time. You can make hacks only if both versions of the problem are solved.</span></p><p>After Zhongkao examination, Daniel and his friends are going to have a party. Everyone will come with some candies.</p><p>There will be $n$ people at the party. Initially, the $i$-th person has $a_i$ candies. During the party, they will swap their candies. To do this, they will line up <span class="tex-font-style-bf">in an arbitrary order</span> and everyone will do the following <span class="tex-font-style-bf">exactly once</span>:</p><ul> <li> Choose an integer $p$ ($1 \le p \le n$) and a <span class="tex-font-style-bf">non-negative</span> integer $x$, then give his $2^{x}$ candies to the $p$-th person. Note that one <span class="tex-font-style-bf">cannot</span> give more candies than currently he has (he might receive candies from someone else before) and he <span class="tex-font-style-bf">cannot</span> give candies to himself. </li></ul><p>Daniel likes fairness, so he will be happy if and only if everyone receives candies from <span class="tex-font-style-bf">exactly one person</span>. Meanwhile, his friend Tom likes average, so he will be happy if and only if all the people have the same number of candies after all swaps.</p><p>Determine whether there exists a way to swap candies, so that both Daniel and Tom will be happy after the swaps.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1\le t\le 1000$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\le n\le 2\cdot 10^5$) — the number of people at the party.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\le 10^9$) — the number of candies each person has.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print "<span class="tex-font-style-tt">Yes</span>" (without quotes) if exists a way to swap candies to make both Daniel and Tom happy, and print "<span class="tex-font-style-tt">No</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1\le t\le 1000$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\le n\le 2\cdot 10^5$) — the number of people at the party.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\le 10^9$) — the number of candies each person has.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, print "<span class="tex-font-style-tt">Yes</span>" (without quotes) if exists a way to swap candies to make both Daniel and Tom happy, and print "<span class="tex-font-style-tt">No</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,6,7,10,11
6
3
2 4 3
5
1 2 3 4 5
6
1 4 7 1 5 4
2
20092043 20092043
12
9 9 8 2 4 4 3 5 1 1 1 1
6
2 12 7 16 11 12
```




```output1
Yes
Yes
No
Yes
No
No
```



## Note

<p>In the first test case:</p><ul> <li> The first person gives $1$ candy to the third person; </li><li> The second person gives $2$ candies to the first person; </li><li> The third person gives $1$ candy to the second person. </li></ul><p>Then all people have $3$ candies.</p><p>In the second test case:</p><ul> <li> The fifth person gives $4$ candies to the first person, from now on the first person has $5$ candies; </li><li> The first person gives $2$ candies to the third person; </li><li> The third person gives $2$ candies to the fifth person; </li><li> The fourth person gives $2$ candies to the second person; </li><li> The second person gives $1$ candy to the fourth person. </li></ul><p>Then all people have $3$ candies. Note that at first the first person cannot give $2$ candies to the third person, since he only has $a_1=1$ candy. But after the fifth person gives him $4$ candies, he can do this, because he currently has $1+4=5$ candies.</p><p>In the third test case, it's impossible for all people to have the same number of candies.</p><p>In the fourth test case, the first person gives $1024$ candies to the second person, and the second person gives $1024$ candies to the first person as well.</p>
