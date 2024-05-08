## Description

<div><p>You are given a book with $n$ chapters.</p><p>Each chapter has a specified list of other chapters that need to be understood in order to understand this chapter. To understand a chapter, you must read it after you understand every chapter on its required list.</p><p>Currently you don't understand any of the chapters. You are going to read the book from the beginning till the end repeatedly until you understand the whole book. Note that if you read a chapter at a moment when you don't understand some of the required chapters, you don't understand this chapter.</p><p>Determine how many times you will read the book to understand every chapter, or determine that you will never understand every chapter no matter how many times you read the book.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2\cdot10^4$).</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2\cdot10^5$) — number of chapters.</p><p>Then $n$ lines follow. The $i$-th line begins with an integer $k_i$ ($0 \le k_i \le n-1$) — number of chapters required to understand the $i$-th chapter. Then $k_i$ integers $a_{i,1}, a_{i,2}, \dots, a_{i, k_i}$ ($1 \le a_{i, j} \le n, a_{i, j} \ne i, a_{i, j} \ne a_{i, l}$ for $j \ne l$) follow — the chapters required to understand the $i$-th chapter.</p><p>It is guaranteed that the sum of $n$ and sum of $k_i$ over all testcases do not exceed $2\cdot10^5$.</p></div><div class="output-specification"><p>For each test case, if the entire book can be understood, print how many times you will read it, otherwise print $-1$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2\cdot10^4$).</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2\cdot10^5$) — number of chapters.</p><p>Then $n$ lines follow. The $i$-th line begins with an integer $k_i$ ($0 \le k_i \le n-1$) — number of chapters required to understand the $i$-th chapter. Then $k_i$ integers $a_{i,1}, a_{i,2}, \dots, a_{i, k_i}$ ($1 \le a_{i, j} \le n, a_{i, j} \ne i, a_{i, j} \ne a_{i, l}$ for $j \ne l$) follow — the chapters required to understand the $i$-th chapter.</p><p>It is guaranteed that the sum of $n$ and sum of $k_i$ over all testcases do not exceed $2\cdot10^5$.</p>

## Output

<p>For each test case, if the entire book can be understood, print how many times you will read it, otherwise print $-1$.</p>





```input1
5
4
1 2
0
2 1 4
1 2
5
1 5
1 1
1 2
1 3
1 4
5
0
0
2 1 2
1 2
2 2 1
4
2 2 3
0
0
2 3 2
5
1 2
1 3
1 4
1 5
0
```




```output1
2
-1
1
2
5
```



## Note

<p>In the first example, we will understand chapters $\{2, 4\}$ in the first reading and chapters $\{1, 3\}$ in the second reading of the book.</p><p>In the second example, every chapter requires the understanding of some other chapter, so it is impossible to understand the book.</p><p>In the third example, every chapter requires only chapters that appear earlier in the book, so we can understand everything in one go.</p><p>In the fourth example, we will understand chapters $\{2, 3, 4\}$ in the first reading and chapter $1$ in the second reading of the book.</p><p>In the fifth example, we will understand one chapter in every reading from $5$ to $1$.</p>
