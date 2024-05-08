## Description

<div><p>Tenzing received $3n$ books from his fans. The books are arranged in $3$ stacks with $n$ books in each stack. Each book has a non-negative integer difficulty rating.</p><p>Tenzing wants to read some (possibly zero) books. At first, his <span class="tex-font-style-it">knowledge</span> is $0$.</p><p>To read the books, Tenzing will choose a non-empty stack, read the book on the top of the stack, and then discard the book. If Tenzing's knowledge is currently $u$, then his knowledge will become $u|v$ after reading a book with difficulty rating $v$. Here $|$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#OR">bitwise OR operation</a>. Note that Tenzing can stop reading books whenever he wants.</p><p>Tenzing's favourite number is $x$. Can you help Tenzing check if it is possible for his knowledge to become $x$?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $x$ ($1 \leq n \leq 10^5$, $0 \leq x \leq 10^9$)&nbsp;— the number of books in each stack and Tenzing's favourite number.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($0 \leq a_i \leq 10^9$) &nbsp;— the difficulty rating of the books in the first stack, from top to bottom.</p><p>The third line of each test case contains $n$ integers $b_1,b_2,\ldots,b_n$ ($0 \leq b_i \leq 10^9$) &nbsp;— the difficulty rating of the books in the second stack, from top to bottom.</p><p>The fourth line of each test case contains $n$ integers $c_1,c_2,\ldots,c_n$ ($0 \leq c_i \leq 10^9$) &nbsp;— the difficulty rating of the books in the third stack, from top to bottom.</p><p>It is guaranteed that the sum of $n$ does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">Yes</span>" (without quotes) if Tenzing can make his knowledge equal to $x$, and "<span class="tex-font-style-tt">No</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $x$ ($1 \leq n \leq 10^5$, $0 \leq x \leq 10^9$)&nbsp;— the number of books in each stack and Tenzing's favourite number.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($0 \leq a_i \leq 10^9$) &nbsp;— the difficulty rating of the books in the first stack, from top to bottom.</p><p>The third line of each test case contains $n$ integers $b_1,b_2,\ldots,b_n$ ($0 \leq b_i \leq 10^9$) &nbsp;— the difficulty rating of the books in the second stack, from top to bottom.</p><p>The fourth line of each test case contains $n$ integers $c_1,c_2,\ldots,c_n$ ($0 \leq c_i \leq 10^9$) &nbsp;— the difficulty rating of the books in the third stack, from top to bottom.</p><p>It is guaranteed that the sum of $n$ does not exceed $10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">Yes</span>" (without quotes) if Tenzing can make his knowledge equal to $x$, and "<span class="tex-font-style-tt">No</span>" (without quotes) otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,4,5,10,11,12,13
3
5 7
1 2 3 4 5
5 4 3 2 1
1 3 5 7 9
5 2
3 2 3 4 5
5 4 3 2 1
3 3 5 7 9
3 0
1 2 3
3 2 1
2 2 2
```




```output1
Yes
No
Yes
```



## Note

<p>For the first test case, Tenzing can read the following $4$ books: </p><ul> <li> read the book with difficulty rating $1$ on the top of the first stack. Tenzing's knowledge changes to $0|1=1$. </li><li> read the book with difficulty rating $1$ on the top of the third stack. Tenzing's knowledge changes to $1|1=1$. </li><li> read the book with difficulty rating $2$ on the top of the first stack. Tenzing's knowledge changes to $1|2=3$. </li><li> read the book with difficulty rating $5$ on the top of the second stack. Tenzing's knowledge changes to $3|5=7$. </li></ul><p>After reading all books, Tenzing's knowledge is $7$.</p><p>For the third test case, Tenzing can read $0$ books to make his final knowledge equals to $0$.</p>
