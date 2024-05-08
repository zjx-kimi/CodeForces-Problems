## Description

<div><p>When Valera has got some free time, he goes to the library to read some books. Today he's got <span class="tex-span"><i>t</i></span> free minutes to read. That's why Valera took <span class="tex-span"><i>n</i></span> books in the library and for each book he estimated the time he is going to need to read it. Let's number the books by integers from 1 to <span class="tex-span"><i>n</i></span>. Valera needs <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> minutes to read the <span class="tex-span"><i>i</i></span>-th book.</p><p>Valera decided to choose an arbitrary book with number <span class="tex-span"><i>i</i></span> and read the books one by one, starting from this book. In other words, he will first read book number <span class="tex-span"><i>i</i></span>, then book number <span class="tex-span"><i>i</i> + 1</span>, then book number <span class="tex-span"><i>i</i> + 2</span> and so on. He continues the process until he either runs out of the free time or finishes reading the <span class="tex-span"><i>n</i></span>-th book. Valera reads each book up to the end, that is, he doesn't start reading the book if he doesn't have enough free time to finish reading it. </p><p>Print the maximum number of books Valera can read.</p></div><div class="input-specification"><p>The first line contains two integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>t</i></span> <span class="tex-span">(1 ≤ <i>n</i> ≤ 10<sup class="upper-index">5</sup>;&nbsp;1 ≤ <i>t</i> ≤ 10<sup class="upper-index">9</sup>)</span> — the number of books and the number of free minutes Valera's got. The second line contains a sequence of <span class="tex-span"><i>n</i></span> integers <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>, <i>a</i><sub class="lower-index">2</sub>, ..., <i>a</i><sub class="lower-index"><i>n</i></sub></span> <span class="tex-span">(1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub> ≤ 10<sup class="upper-index">4</sup>)</span>, where number <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> shows the number of minutes that the boy needs to read the <span class="tex-span"><i>i</i></span>-th book.</p></div><div class="output-specification"><p>Print a single integer — the maximum number of books Valera can read.</p></div>

## Input

<p>The first line contains two integers <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>t</i></span> <span class="tex-span">(1 ≤ <i>n</i> ≤ 10<sup class="upper-index">5</sup>;&nbsp;1 ≤ <i>t</i> ≤ 10<sup class="upper-index">9</sup>)</span> — the number of books and the number of free minutes Valera's got. The second line contains a sequence of <span class="tex-span"><i>n</i></span> integers <span class="tex-span"><i>a</i><sub class="lower-index">1</sub>, <i>a</i><sub class="lower-index">2</sub>, ..., <i>a</i><sub class="lower-index"><i>n</i></sub></span> <span class="tex-span">(1 ≤ <i>a</i><sub class="lower-index"><i>i</i></sub> ≤ 10<sup class="upper-index">4</sup>)</span>, where number <span class="tex-span"><i>a</i><sub class="lower-index"><i>i</i></sub></span> shows the number of minutes that the boy needs to read the <span class="tex-span"><i>i</i></span>-th book.</p>

## Output

<p>Print a single integer — the maximum number of books Valera can read.</p>





```input1
4 5
3 1 2 1

```




```input2
3 3
2 2 3

```




```output1
3

```




```output2
1

```


