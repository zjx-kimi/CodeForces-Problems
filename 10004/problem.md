## Description

<div><p>Vladislav has $n$ cards numbered $1, 2, \dots, n$. He wants to lay them down in a row as follows: </p><ul> <li> First, he lays down all the odd-numbered cards from smallest to largest. </li><li> Next, he lays down all cards that are twice an odd number from smallest to largest (i.e. $2$ multiplied by an odd number). </li><li> Next, he lays down all cards that are $3$ times an odd number from smallest to largest (i.e. $3$ multiplied by an odd number). </li><li> Next, he lays down all cards that are $4$ times an odd number from smallest to largest (i.e. $4$ multiplied by an odd number). </li><li> And so on, until all cards are laid down. </li></ul> What is the $k$-th card he lays down in this process? Once Vladislav puts a card down, he cannot use that card again.</div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \leq t \leq 5 \cdot 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains two integers $n$ and $k$ ($1 \leq k \leq n \leq 10^9$)&nbsp;— the number of cards Vlad has, and the position of the card you need to output.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the $k$-th card Vladislav lays down.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \leq t \leq 5 \cdot 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains two integers $n$ and $k$ ($1 \leq k \leq n \leq 10^9$)&nbsp;— the number of cards Vlad has, and the position of the card you need to output.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the $k$-th card Vladislav lays down.</p>





```input1|2,4,6,8,10,12
11
7 1
7 2
7 3
7 4
7 5
7 6
7 7
1 1
34 14
84 19
1000000000 1000000000
```




```output1
1
3
5
7
2
6
4
1
27
37
536870912
```



## Note

<p>In the first seven test cases, $n=7$. Vladislav lays down the cards as follows: </p><ul> <li> First&nbsp;— all the odd-numbered cards in the order $1$, $3$, $5$, $7$. </li><li> Next&nbsp;— all cards that are twice an odd number in the order $2$, $6$. </li><li> Next, there are no remaining cards that are $3$ times an odd number. (Vladislav has only one of each card.) </li><li> Next&nbsp;— all cards that are $4$ times an odd number, and there is only one such card: $4$. </li><li> There are no more cards left, so Vladislav stops. </li></ul> Thus the order of cards is $1$, $3$, $5$, $7$, $2$, $6$, $4$.
