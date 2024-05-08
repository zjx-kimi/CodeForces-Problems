## Description

<div><p>In the evenings during the hike, Kirill and Anton decided to take out an array of integers $a$ of length $n$ from their backpack and play a game with it. The rules are as follows:</p><ol><li> Kirill chooses from $2$ to $(n-2)$ numbers and encircles them in red.</li><li> Anton encircles all the remaining numbers in blue.</li><li> Kirill calculates the <span class="tex-font-style-bf">greatest common divisor</span> (<a href="https://en.wikipedia.org/wiki/Greatest_common_divisor">GCD</a>) of all the red numbers.</li><li> Anton calculates the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#AND"><span class="tex-font-style-bf">bitwise AND</span></a> of all the blue numbers and adds the number $x$ to the result.</li><li> If the GCD of all the red numbers is strictly greater than the sum of the bitwise AND of all the blue numbers and the number $x$, then Kirill wins; otherwise, Anton wins.</li></ol><p>Help Kirill to beat Anton or tell if it's impossible.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 20\,000$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $x$ ($4\le n \le 4\cdot 10^5$, $0 \le x \le 4\cdot 10^5$)&nbsp;— the number of integers and the number $x$ respectively.</p><p>The second line contains an array $a$ of length $n$ ($1 \le a_i \le 4\cdot 10^5$).</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $4\cdot 10^5$. It is also guaranteed that the sum of the maximum values of $a_i$ for each test case does not exceed $4\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" on the first line if the condition can be met, on the second line, output the number of chosen numbers by Kirill and the numbers themselves in any order separated by a space, and on the third line, output the size of the second set and the numbers in it.</p><p>Otherwise, output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 20\,000$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $x$ ($4\le n \le 4\cdot 10^5$, $0 \le x \le 4\cdot 10^5$)&nbsp;— the number of integers and the number $x$ respectively.</p><p>The second line contains an array $a$ of length $n$ ($1 \le a_i \le 4\cdot 10^5$).</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $4\cdot 10^5$. It is also guaranteed that the sum of the maximum values of $a_i$ for each test case does not exceed $4\cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" on the first line if the condition can be met, on the second line, output the number of chosen numbers by Kirill and the numbers themselves in any order separated by a space, and on the third line, output the size of the second set and the numbers in it.</p><p>Otherwise, output "<span class="tex-font-style-tt">NO</span>".</p><p>You can output each letter in any case (lowercase or uppercase). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be accepted as a positive answer.</p>





```input1|2,3,6,7,10,11,14,15
8
4 1
4 3 1 8
4 1
4 5 8 4
5 0
1 1 1 1 1
5 2
31 63 127 63 31
4 1
1 3 3 3
8 3
4 3 4 1 2 2 5 3
4 2
1 4 3 6
8 48
31 61 37 15 53 26 61 12
```




```output1
YES
2 4 8
2 3 1 
YES
2 4 4
2 5 8 
NO
YES
2 63 63
3 31 127 31
YES
2 3 3
2 1 3
YES
2 4 4
6 3 1 2 2 5 3
YES
2 3 6
2 1 4 
YES
2 61 61
6 31 37 15 53 26 12
```


