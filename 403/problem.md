## Description

<div><p>Petya is an administrator of a channel in one of the messengers. A total of $n$ people are subscribed to his channel, and Petya is not considered a subscriber.</p><p>Petya has published a new post on the channel. At the moment of the publication, there were $a$ subscribers online. We assume that every subscriber always reads all posts in the channel if they are online.</p><p>After this, Petya starts monitoring the number of subscribers online. He consecutively receives $q$ notifications of the form "a subscriber went offline" or "a subscriber went online". Petya does not know which exact subscriber goes online or offline. It is guaranteed that such a sequence of notifications could have indeed been received.</p><p>Petya wonders if all of his subscribers have read the new post. Help him by determining one of the following: </p><ul> <li> it is impossible that all $n$ subscribers have read the post; </li><li> it is possible that all $n$ subscribers have read the post; </li><li> it is guaranteed that all $n$ subscribers have read the post. </li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 500$). The description of the test cases follows.</p><p>The first line of each test case contains three integers $n$, $a$, and $q$ ($1 \le n \le 100$, $0 \le a \le n$, $1 \le q \le 100$)&nbsp;— the number of subscribers of the channel, the initial number of subscribers online, and the number of notifications.</p><p>The second line of each test case contains a string of length $q$, consisting of characters '<span class="tex-font-style-tt">+</span>' and '<span class="tex-font-style-tt">-</span>'. The $i$-th of these characters is '<span class="tex-font-style-tt">+</span>', if the $i$-th notification tells that a subscriber goes online, and it is '<span class="tex-font-style-tt">-</span>' otherwise.</p></div><div class="output-specification"><p>For each test case, output a single line: "<span class="tex-font-style-tt">YES</span>" if all $n$ subscribers are guaranteed to have read the post, "<span class="tex-font-style-tt">NO</span>" if it is impossible for all $n$ subscribers to have read the post, and "<span class="tex-font-style-tt">MAYBE</span>" otherwise.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 500$). The description of the test cases follows.</p><p>The first line of each test case contains three integers $n$, $a$, and $q$ ($1 \le n \le 100$, $0 \le a \le n$, $1 \le q \le 100$)&nbsp;— the number of subscribers of the channel, the initial number of subscribers online, and the number of notifications.</p><p>The second line of each test case contains a string of length $q$, consisting of characters '<span class="tex-font-style-tt">+</span>' and '<span class="tex-font-style-tt">-</span>'. The $i$-th of these characters is '<span class="tex-font-style-tt">+</span>', if the $i$-th notification tells that a subscriber goes online, and it is '<span class="tex-font-style-tt">-</span>' otherwise.</p>

## Output

<p>For each test case, output a single line: "<span class="tex-font-style-tt">YES</span>" if all $n$ subscribers are guaranteed to have read the post, "<span class="tex-font-style-tt">NO</span>" if it is impossible for all $n$ subscribers to have read the post, and "<span class="tex-font-style-tt">MAYBE</span>" otherwise.</p>





```input1|2,3,6,7
4
5 5 3
--+
5 2 3
++-
5 4 2
-+
5 0 7
++++-++
```




```output1
YES
NO
MAYBE
YES
```



## Note

<p>In the first test case, there are $5$ out of $5$ subscribers online in the very beginning, so they will all read the post no matter what. The answer is "<span class="tex-font-style-tt">YES</span>".</p><p>In the second test case, the number of subscribers online becomes $4$ after the first two notifications, next someone goes offline, and thus the fifth subscriber has no chance of reading the post. It is impossible for all the subscribers to read the post, so the answer is "<span class="tex-font-style-tt">NO</span>".</p><p>In the third test case, on the one hand, the same person may have gone offline and online (in this case only $4$ out of $5$ subscribers have read the post), on the other hand, the last notification may have told that the fifth subscriber has gone online (in this case all subscribers have read the post). We cannot deduce which of the two holds, so the answer is "<span class="tex-font-style-tt">MAYBE</span>".</p><p>In the fourth test case, there have to be five subscribers online after all the notifications. All of them will read the post, so the answer is "<span class="tex-font-style-tt">YES</span>".</p>
