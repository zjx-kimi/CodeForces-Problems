## Description

<div><p>Mushroom Filippov cooked himself a meal and while having his lunch, he decided to watch a video on <span class="tex-font-style-tt">TubeTube</span>. He can not spend more than $t$ seconds for lunch, so he asks you for help with the selection of video.</p><p>The <span class="tex-font-style-tt">TubeTube</span> feed is a list of $n$ videos, indexed from $1$ to $n$. The $i$-th video lasts $a_i$ seconds and has an entertainment value $b_i$. Initially, the feed is opened on the first video, and Mushroom can skip to the next video in $1$ second (if the next video exists). Mushroom can skip videos any number of times (including zero).</p><p>Help Mushroom choose <span class="tex-font-style-bf">one</span> video that he can open and watch in $t$ seconds. If there are several of them, he wants to choose the most entertaining one. Print the index of any appropriate video, or $-1$ if there is no such.</p></div><div class="input-specification"><p>The first line of the input data contains a single integer $q$ ($1 \le q \le 1000$)&nbsp;— the number of test cases in the test.</p><p>The description of the test cases follows.</p><p>The first line of a test case contains two integers $n$ and $t$ ($1 \le n \le 50$, $1 \le t \le 200$)&nbsp;— the number of videos in the feed and seconds for lunch, respectively.</p><p>The second line of a test case contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($1 \le a_i \le 100$)&nbsp;— durations of videos. </p><p>The third line of a test case contains $n$ integers $b_1, b_2, b_3, \dots, b_n$ ($1 \le b_i \le 100$)&nbsp;— entertainment values of videos.</p></div><div class="output-specification"><p>Output $q$ integers, each of which is the answer to the corresponding test case. As an answer, output the <span class="tex-font-style-bf">index</span> of the most entertaining video that Mushroom will have time to watch. If there are several answers, you are allowed to output any of them. Output $-1$, if there is no video he can watch during his lunch break.</p></div>

## Input

<p>The first line of the input data contains a single integer $q$ ($1 \le q \le 1000$)&nbsp;— the number of test cases in the test.</p><p>The description of the test cases follows.</p><p>The first line of a test case contains two integers $n$ and $t$ ($1 \le n \le 50$, $1 \le t \le 200$)&nbsp;— the number of videos in the feed and seconds for lunch, respectively.</p><p>The second line of a test case contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($1 \le a_i \le 100$)&nbsp;— durations of videos. </p><p>The third line of a test case contains $n$ integers $b_1, b_2, b_3, \dots, b_n$ ($1 \le b_i \le 100$)&nbsp;— entertainment values of videos.</p>

## Output

<p>Output $q$ integers, each of which is the answer to the corresponding test case. As an answer, output the <span class="tex-font-style-bf">index</span> of the most entertaining video that Mushroom will have time to watch. If there are several answers, you are allowed to output any of them. Output $-1$, if there is no video he can watch during his lunch break.</p>





```input1|2,3,4,8,9,10,14,15,16
5
5 9
1 5 7 6 6
3 4 7 1 9
4 4
4 3 3 2
1 2 3 4
5 7
5 5 5 5 5
2 1 3 9 7
4 33
54 71 69 96
42 24 99 1
2 179
55 66
77 88
```




```output1
3
2
3
-1
2
```


