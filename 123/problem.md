## Description

<div><p>Monocarp is a security guard in Berland State University. Every day, he tracks how many people and at what time enter and leave the university. He writes this information down as follows: </p><ul> <li> when someone enters the university, Monocarp writes a plus sign '<span class="tex-font-style-tt">+</span>'; </li><li> when someone leaves the university, Monocarp writes a minus sign '<span class="tex-font-style-tt">-</span>'. </li></ul><p>At the beginning of the current day, there are no people at the university, except for Monocarp. During the day, Monocarp wrote out a sequence $s$. The characters in $s$ are listed in the order Monocarp wrote them.</p><p>Suddenly, Monocarp's boss decided to check his work. Unfortunately, Monocarp is a bit careless. So, the sequence $s$ that he wrote might be impossible. For example, the sequence "<span class="tex-font-style-tt">+-</span><span class="tex-font-style-tt">-</span>" can't happen, since it represents a scenario when one person enters the university and two leave.</p><p>Before his boss starts checking the sequence, Monocarp has the time to swap at most one pair of characters in it. Can he do it in such a way that the resulting sequence is plausible? Note that if the given sequence is already plausible, Monocarp doesn't have to swap anything.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single string $s$ ($1 \le |s| \le 3 \cdot 10^5$), consisting only of characters '<span class="tex-font-style-tt">+</span>' and/or '<span class="tex-font-style-tt">-</span>'. A plus sign '<span class="tex-font-style-tt">+</span>' represents a person entering the university. A minus sign '<span class="tex-font-style-tt">-</span>' represents a person leaving the university.</p><p>The sum of all $|s|$ over all test cases doesn't exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print an answer.</p><p>If it's impossible to swap at most one pair of characters so that the resulting sequence is plausible, print <span class="tex-font-style-tt">-1</span>.</p><p>Otherwise, print two integers. If you swap one pair of characters, print two distinct integers from $1$ to $n$&nbsp;— the indices of characters to swap. If you don't swap, print one integer from $1$ to $n$ twice&nbsp;— swap a character with itself.</p><p>If there are multiple answers, print any of them.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single string $s$ ($1 \le |s| \le 3 \cdot 10^5$), consisting only of characters '<span class="tex-font-style-tt">+</span>' and/or '<span class="tex-font-style-tt">-</span>'. A plus sign '<span class="tex-font-style-tt">+</span>' represents a person entering the university. A minus sign '<span class="tex-font-style-tt">-</span>' represents a person leaving the university.</p><p>The sum of all $|s|$ over all test cases doesn't exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print an answer.</p><p>If it's impossible to swap at most one pair of characters so that the resulting sequence is plausible, print <span class="tex-font-style-tt">-1</span>.</p><p>Otherwise, print two integers. If you swap one pair of characters, print two distinct integers from $1$ to $n$&nbsp;— the indices of characters to swap. If you don't swap, print one integer from $1$ to $n$ twice&nbsp;— swap a character with itself.</p><p>If there are multiple answers, print any of them.</p>





```input1|2,4,6
6
-+
+-
+++-
---++
+
-
```




```output1
1 2
1 1
1 1
-1
1 1
-1
```


