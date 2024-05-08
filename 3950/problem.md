## Description

<div><p><span class="tex-font-style-bf"><span class="tex-font-style-it">The only difference between easy and hard versions is constraints.</span></span></p><p>Polycarp loves to listen to music, so he never leaves the player, even on the way home from the university. Polycarp overcomes the distance from the university to the house in exactly $T$ minutes.</p><p>In the player, Polycarp stores $n$ songs, each of which is characterized by two parameters: $t_i$ and $g_i$, where $t_i$ is the length of the song in minutes ($1 \le t_i \le 50$), $g_i$ is its genre ($1 \le g_i \le 3$).</p><p>Polycarp wants to create such a playlist so that he can listen to music all the time on the way from the university to his home, and at the time of his arrival home, the playlist is over. Polycarp never interrupts songs and always listens to them from beginning to end. Thus, if he started listening to the $i$-th song, he would spend exactly $t_i$ minutes on its listening. Polycarp also does not like when two songs of the same genre play in a row (i.e. successively/adjacently) or when the songs in his playlist are repeated.</p><p>Help Polycarpus count the number of different sequences of songs (their order matters), the total duration is exactly $T$, such that there are no two consecutive songs of the same genre in them and all the songs in the playlist are different.</p></div><div class="input-specification"><p>The first line of the input contains two integers $n$ and $T$ ($1 \le n \le 50, 1 \le T \le 2500$) — the number of songs in the player and the required total duration, respectively.</p><p>Next, the $n$ lines contain descriptions of songs: the $i$-th line contains two integers $t_i$ and $g_i$ ($1 \le t_i \le 50, 1 \le g_i \le 3$) — the duration of the $i$-th song and its genre, respectively.</p></div><div class="output-specification"><p>Output one integer — the number of different sequences of songs, the total length of exactly $T$, such that there are no two consecutive songs of the same genre in them and all the songs in the playlist are different. Since the answer may be huge, output it modulo $10^9 + 7$ (that is, the remainder when dividing the quantity by $10^9 + 7$).</p></div>

## Input

<p>The first line of the input contains two integers $n$ and $T$ ($1 \le n \le 50, 1 \le T \le 2500$) — the number of songs in the player and the required total duration, respectively.</p><p>Next, the $n$ lines contain descriptions of songs: the $i$-th line contains two integers $t_i$ and $g_i$ ($1 \le t_i \le 50, 1 \le g_i \le 3$) — the duration of the $i$-th song and its genre, respectively.</p>

## Output

<p>Output one integer — the number of different sequences of songs, the total length of exactly $T$, such that there are no two consecutive songs of the same genre in them and all the songs in the playlist are different. Since the answer may be huge, output it modulo $10^9 + 7$ (that is, the remainder when dividing the quantity by $10^9 + 7$).</p>





```input1
3 3
1 1
1 2
1 3
```




```input2
3 3
1 1
1 1
1 3
```




```input3
4 10
5 3
2 1
3 2
5 1
```




```output1
6
```




```output2
2
```




```output3
10
```



## Note

<p>In the first example, Polycarp can make any of the $6$ possible playlist by rearranging the available songs: $[1, 2, 3]$, $[1, 3, 2]$, $[2, 1, 3]$, $[2, 3, 1]$, $[3, 1, 2]$ and $[3, 2, 1]$ (indices of the songs are given).</p><p>In the second example, the first and second songs cannot go in succession (since they have the same genre). Thus, Polycarp can create a playlist in one of $2$ possible ways: $[1, 3, 2]$ and $[2, 3, 1]$ (indices of the songs are given).</p><p>In the third example, Polycarp can make the following playlists: $[1, 2, 3]$, $[1, 3, 2]$, $[2, 1, 3]$, $[2, 3, 1]$, $[3, 1, 2]$, $[3, 2, 1]$, $[1, 4]$, $[4, 1]$, $[2, 3, 4]$ and $[4, 3, 2]$ (indices of the songs are given).</p>
