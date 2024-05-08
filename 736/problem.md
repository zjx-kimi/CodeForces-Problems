## Description

<div> The boy Vitya loves to listen to music very much. He knows that $n$ albums are due to be released this Friday, $i$-th of which contains $k_i$ tracks. Of course, Vitya has already listened to all the tracks, and knows that in the $i$-th album, the coolness of the $j$-th track is equal to $a_{i,j}$.<p>Vitya has a friend Masha, whom he really wants to invite to the festival, where his favorite bands perform. However, in order for a friend to agree, she must first evaluate the released novelties. Vitya knows that if Masha listens to a track that was cooler than all the previous ones, she will get 1 unit of impression. Unfortunately, albums can only be listened to in their entirety, without changing the songs in them in places.</p><p>Help Vitya find such an order of albums so that Masha's impression turns out to be as much as possible, and she definitely went to the festival with him. </p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer t ($1 \le t \le 200\,000$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 200\,000$)&nbsp;— number of albums.</p><p>The album descriptions follow. Each album description consists of two lines:</p><p>The first line contains a single integer $k_i$ ($1 \le k_i \le 200\,000$)&nbsp;— the number of tracks in the $i$th album.</p><p>The following line contains $k_i$ integers $a_{i, 1},\ a_{i, 2},\ a_{i, 3},\ \ldots,\ a_{i, k_i}$ ($1 \le a_{i,j} \le 200\,000$)&nbsp;— the coolness of the tracks in the $i$ album. </p><p>Denote for $\sum k_i$ the sum of all $k_i$. It is guaranteed that $\sum k_i \le 200\,000$. </p></div><div class="output-specification"><p>For each test case print the singular number &nbsp;— the maximum impression that Masha can get. </p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer t ($1 \le t \le 200\,000$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 200\,000$)&nbsp;— number of albums.</p><p>The album descriptions follow. Each album description consists of two lines:</p><p>The first line contains a single integer $k_i$ ($1 \le k_i \le 200\,000$)&nbsp;— the number of tracks in the $i$th album.</p><p>The following line contains $k_i$ integers $a_{i, 1},\ a_{i, 2},\ a_{i, 3},\ \ldots,\ a_{i, k_i}$ ($1 \le a_{i,j} \le 200\,000$)&nbsp;— the coolness of the tracks in the $i$ album. </p><p>Denote for $\sum k_i$ the sum of all $k_i$. It is guaranteed that $\sum k_i \le 200\,000$. </p>

## Output

<p>For each test case print the singular number &nbsp;— the maximum impression that Masha can get. </p>





```input1|2,3,4,5,6,7,8,9,10
2
4
5
4 9 4 6 8
1
7
2
8 6
1
1
4
2
3 4
2
1 8
2
2 8
2
7 9
```




```output1
4
4
```



## Note

<p>In the first test example, the optimal order is listening to the 4th, 2nd, 3rd and 1st albums. </p><p>In this case, Masha will listen to the tracks in the following order: <span class="tex-font-style-bf">1</span>; <span class="tex-font-style-bf">7</span>; <span class="tex-font-style-bf">8</span>, 6; 4, <span class="tex-font-style-bf">9</span>, 4, 6, 8 and will receive 4 units of impression.</p><p>In the second test example, you must first listen to the 1st, then the 4th, and in any order the 2nd and 3rd.   In this case, Masha will get the maximum impression, and for every song in the 1st and 4th albums and nothing for the 2nd and 3rd. </p>
