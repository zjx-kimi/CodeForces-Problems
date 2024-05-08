## Description

<div><p><span class="tex-font-style-it">In order to test the hypothesis about the cats, the scientists must arrange the cats in the boxes in a specific way. Of course, they would like to test the hypothesis and publish a sensational article as quickly as possible, because they are too engrossed in the next hypothesis about the phone's battery charge.</span></p><p>Scientists have $n$ boxes in which cats may or may not sit. Let the current state of the boxes be denoted by the sequence $b_1, \dots, b_n$: $b_i = 1$ if there is a cat in box number $i$, and $b_i = 0$ otherwise. </p><p>Fortunately, the unlimited production of cats has already been established, so in one day, the scientists can perform one of the following operations:</p><ul> <li> Take a new cat and place it in a box (for some $i$ such that $b_i = 0$, assign $b_i = 1$). </li><li> Remove a cat from a box and send it into retirement (for some $i$ such that $b_i = 1$, assign $b_i = 0$). </li><li> Move a cat from one box to another (for some $i, j$ such that $b_i = 1, b_j = 0$, assign $b_i = 0, b_j = 1$). </li></ul><p>It has also been found that some boxes were immediately filled with cats. Therefore, the scientists know the initial position of the cats in the boxes $s_1, \dots, s_n$ and the desired position $f_1, \dots, f_n$.</p><p>Due to the large amount of paperwork, the scientists do not have time to solve this problem. Help them for the sake of science and indicate the minimum number of days required to test the hypothesis.</p></div><div class="input-specification"><p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. This is followed by descriptions of the test cases.</p><p>Each test case consists of three lines.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of boxes.</p><p>The second line of each test case contains a string $s$ of $n$ characters, where the $i$-th character is '1' if there is a cat in the $i$-th box and '0' otherwise.</p><p>The third line of each test case contains a string $f$ of $n$ characters, where the $i$-th character is '1' if there should be a cat in the $i$-th box and '0' otherwise.</p><p>It is guaranteed that in a test the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer on a separate line — the minimum number of operations required to obtain the desired position from the initial position. It can be shown that a solution always exists.</p></div>

## Input

<p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. This is followed by descriptions of the test cases.</p><p>Each test case consists of three lines.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of boxes.</p><p>The second line of each test case contains a string $s$ of $n$ characters, where the $i$-th character is '1' if there is a cat in the $i$-th box and '0' otherwise.</p><p>The third line of each test case contains a string $f$ of $n$ characters, where the $i$-th character is '1' if there should be a cat in the $i$-th box and '0' otherwise.</p><p>It is guaranteed that in a test the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single integer on a separate line — the minimum number of operations required to obtain the desired position from the initial position. It can be shown that a solution always exists.</p>





```input1|2,3,4,8,9,10,14,15,16
6
5
10010
00001
1
1
1
3
000
111
4
0101
1010
3
100
101
8
10011001
11111110
```




```output1
2
0
3
2
1
4
```



## Note

<p>In the first test case, you can first move the cat from the first box to the fifth, and then remove the cat from the fourth box.</p><p>In the second test case, there is nothing to do — the only cat is already sitting in the correct box.</p><p>In the third test case of input data, it takes three days to place a cat in each box.</p>
