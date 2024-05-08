## Description

<div><p>One of the SWERC judges has a dog named Boy. Besides being a good competitive programmer, Boy loves fresh air, so she wants to be walked at least twice a day. Walking Boy requires $120$ <span class="tex-font-style-bf">consecutive</span> minutes. Two walks cannot overlap, but one can start as soon as the previous one has finished.</p><center> <img class="tex-graphics" src="file://7XLEUHhL.png" style="max-width: 100.0%;max-height: 100.0%;" width="340px"><p>Boy before and after getting ACCEPTED on this problem. </p></center><p>Today, the judge sent $n$ messages to the SWERC Discord server. The $i$-th message was sent $a_i$ minutes after midnight. You know that, when walking Boy, the judge does not send any messages, but he can send a message right before or right after a walk. Is it possible that the judge walked Boy at least twice today?</p><p>Note that a day has $1440$ minutes, and a walk is considered to happen <span class="tex-font-style-it">today</span> if it starts at a minute $s \ge 0$ and ends right before a minute $e \le 1440$. In that case, it must hold that $e - s = 120$ and, for every $i = 1, \, 2 \, \dots, \, n$, either $a_i \le s$ or $a_i \ge e$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \le t \le 100$) — the number of test cases. The descriptions of the $t$ test cases follow.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 100$) — the number of messages sent by the judge.</p><p>The second line of each test case contains $n$ integers $a_1, \, a_2, \, \dots, \, a_n$ ($0 \le a_1 &lt; a_2 &lt; \cdots &lt; a_n &lt; 1440$) — the times at which the messages have been sent (in minutes elapsed from midnight).</p></div><div class="output-specification"><p>For each test case, output one line containing $\texttt{YES}$ if it is possible that Boy has been walked at least twice, and $\texttt{NO}$ otherwise.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \le t \le 100$) — the number of test cases. The descriptions of the $t$ test cases follow.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 100$) — the number of messages sent by the judge.</p><p>The second line of each test case contains $n$ integers $a_1, \, a_2, \, \dots, \, a_n$ ($0 \le a_1 &lt; a_2 &lt; \cdots &lt; a_n &lt; 1440$) — the times at which the messages have been sent (in minutes elapsed from midnight).</p>

## Output

<p>For each test case, output one line containing $\texttt{YES}$ if it is possible that Boy has been walked at least twice, and $\texttt{NO}$ otherwise.</p>





```input1|2,3,6,7,10,11
6
14
100 200 300 400 500 600 700 800 900 1000 1100 1200 1300 1400
12
100 200 300 400 600 700 800 900 1100 1200 1300 1400
13
100 200 300 400 500 600 700 800 900 1100 1200 1300 1400
13
101 189 272 356 463 563 659 739 979 1071 1170 1274 1358
1
42
5
0 1 2 3 4
```




```output1
NO
YES
NO
YES
YES
YES
```



## Note

<p>In the <span class="tex-font-style-bf">first test case</span>, the judge has sent a message at each time multiple of $100$ (excluding $0$). It is impossible that he has walked Boy even once.</p><p>In the <span class="tex-font-style-bf">second test case</span>, the times are the same as above, but $500$ and $1000$ are missing. The judge could have walked Boy, for instance, during the time intervals $[440, 560]$ and $[980, 1100]$. The situation is illustrated in the picture below, where the walks are represented by green intervals.</p><center> <img class="tex-graphics" src="file://J9oqGxV2.png" style="max-width: 100.0%;max-height: 100.0%;" width="605px"> </center><p>$$$$</p><p>In the <span class="tex-font-style-bf">third test case</span>, the times are the same as in the first test case, but $1000$ is missing. The judge could have walked Boy at most once.</p><p>In the <span class="tex-font-style-bf">fourth test case</span>, Boy could have been walked during the time intervals $[739, 859]$ and $[859, 979]$.</p><center> <img class="tex-graphics" src="file://tU13lOua.png" style="max-width: 100.0%;max-height: 100.0%;" width="605px"> </center>
