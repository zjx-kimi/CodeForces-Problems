## Description

<div><p>You are given an array of $n$ integers, where each integer is either $0$, $1$, or $2$. Initially, each element of the array is blue.</p><p>Your goal is to paint each element of the array red. In order to do so, you can perform operations of two types:</p><ul> <li> pay one coin to choose a blue element and paint it red; </li><li> choose a red element which is not equal to $0$ and a blue element <span class="tex-font-style-bf">adjacent</span> to it, decrease the chosen red element by $1$, and paint the chosen blue element red. </li></ul><p>What is the minimum number of coins you have to spend to achieve your goal?</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 2$).</p></div><div class="output-specification"><p>Print one integer — the minimum number of coins you have to spend in order to paint all elements red.</p></div>

## Input

<p>The first line contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 2$).</p>

## Output

<p>Print one integer — the minimum number of coins you have to spend in order to paint all elements red.</p>





```input1
3
0 2 0
```




```input2
4
0 0 1 1
```




```input3
7
0 1 0 0 1 0 2
```




```output1
1
```




```output2
2
```




```output3
4
```



## Note

<p>In the first example, you can paint all elements red with having to spend only one coin as follows:</p><ol> <li> paint the $2$-nd element red by spending one coin; </li><li> decrease the $2$-nd element by $1$ and paint the $1$-st element red; </li><li> decrease the $2$-nd element by $1$ and paint the $3$-rd element red. </li></ol><p>In the second example, you can paint all elements red spending only two coins as follows:</p><ol> <li> paint the $4$-th element red by spending one coin; </li><li> decrease the $4$-th element by $1$ and paint the $3$-rd element red; </li><li> paint the $1$-st element red by spending one coin; </li><li> decrease the $3$-rd element by $1$ and paint the $2$-nd element red. </li></ol>
