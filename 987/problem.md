## Description

<div><p>Monocarp wants to watch $n$ videos. Each video is only one minute long, but its size may be arbitrary. The $i$-th video has the size $a_i$ megabytes. All videos are published on the Internet. A video should be downloaded before it can be watched. Monocarp has poor Internet connection&nbsp;— it takes exactly $1$ minute to download $1$ megabyte of data, so it will require $a_i$ minutes to download the $i$-th video.</p><p>Monocarp's computer has a hard disk of $m$ megabytes. The disk is used to store the downloaded videos. Once Monocarp starts the download of a video of size $s$, the $s$ megabytes are immediately reserved on a hard disk. If there are less than $s$ megabytes left, the download cannot be started until the required space is freed. Each single video can be stored on the hard disk, since $a_i \le m$ for all $i$. Once the download is started, it cannot be interrupted. It is not allowed to run two or more downloads in parallel.</p><p>Once a video is fully downloaded to the hard disk, Monocarp can watch it. Watching each video takes exactly $1$ minute and does not occupy the Internet connection, so Monocarp can start downloading another video while watching the current one.</p><p>When Monocarp finishes watching a video, he doesn't need it on the hard disk anymore, so he can delete the video, instantly freeing the space it occupied on a hard disk. Deleting a video takes negligible time.</p><p>Monocarp wants to watch all $n$ videos as quickly as possible. The order of watching does not matter, since Monocarp needs to watch all of them anyway. Please calculate the minimum possible time required for that.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1 \le n \le 2 \cdot 10^5$; $1 \le m \le 10^9$) — the number of videos Monocarp wants to watch and the size of the hard disk, respectively. </p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le m$) — the sizes of the videos.</p></div><div class="output-specification"><p>Print one integer&nbsp;— the minimum time required to watch all $n$ videos.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1 \le n \le 2 \cdot 10^5$; $1 \le m \le 10^9$) — the number of videos Monocarp wants to watch and the size of the hard disk, respectively. </p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le m$) — the sizes of the videos.</p>

## Output

<p>Print one integer&nbsp;— the minimum time required to watch all $n$ videos.</p>





```input1
5 6
1 2 3 4 5
```




```input2
5 5
1 2 3 4 5
```




```input3
4 3
1 3 2 3
```




```output1
16
```




```output2
17
```




```output3
12
```


