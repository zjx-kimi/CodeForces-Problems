## Description

<div><p>You are given an array consisting of $n$ integers. Your task is to determine whether it is possible to color all its elements in two colors in such a way that the sums of the elements of both colors have the same parity and each color has at least one element colored.</p><p>For example, if the array is [$1,2,4,3,2,3,5,4$], we can color it as follows: [$\color{blue}{1},\color{blue}{2},\color{red}{4},\color{blue}{3},\color{red}{2},\color{red}{3},\color{red}{5},\color{red}{4}$], where the sum of the blue elements is $6$ and the sum of the red elements is $18$.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>Each test case begins with a line containing an integer $n$ ($2 \le n \le 50$)&nbsp;— the length of the array $a$.</p><p>The next line contains $n$ integers $a_1,a_2, \dots, a_n$ ($1 \le a_i \le 50$)&nbsp;— the elements of the array $a$.</p></div><div class="output-specification"><p>For each test case, output "YES" (without quotes) if it is possible to color the array in two colors in such a way that the sums of the elements of both colors have the same parity and each color has at least one element colored, and "NO" otherwise.</p><p>You can output "Yes" and "No" in any case (for example, the strings "yES", "yes", and "Yes" will be recognized as correct answers).</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>Each test case begins with a line containing an integer $n$ ($2 \le n \le 50$)&nbsp;— the length of the array $a$.</p><p>The next line contains $n$ integers $a_1,a_2, \dots, a_n$ ($1 \le a_i \le 50$)&nbsp;— the elements of the array $a$.</p>

## Output

<p>For each test case, output "YES" (without quotes) if it is possible to color the array in two colors in such a way that the sums of the elements of both colors have the same parity and each color has at least one element colored, and "NO" otherwise.</p><p>You can output "Yes" and "No" in any case (for example, the strings "yES", "yes", and "Yes" will be recognized as correct answers).</p>





```input1|2,3,6,7,10,11,14,15
7
8
1 2 4 3 2 3 5 4
2
4 7
3
3 9 8
2
1 7
5
5 4 3 2 1
4
4 3 4 5
2
50 48
```




```output1
YES
NO
YES
YES
NO
YES
YES
```



## Note

<p>The first sample is described in the statement.</p><p>In the second sample, there are only two colorings $[\color{blue}{4},\color{red}{7}]$ and $[\color{red}{4},\color{blue}{7}]$ , but in both cases the parity of sums is different.</p><p>In the third sample, you can color $[\color{blue}{3},\color{blue}{9},\color{red}{8}]$ and $12$ and $8$ are both even.</p>
