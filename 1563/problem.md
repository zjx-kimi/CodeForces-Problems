## Description

<div><p>Distributing budgeted money with limited resources and many constraints is a hard problem. A <span class="tex-font-style-it">budget plan</span> consists of $t$ topics; $i$-th topic consists of $n_i$ items. For each topic, the <span class="tex-font-style-it">optimal relative money distribution</span> is known. The optimal relative distribution for the topic $i$ is a list of real numbers $p_{i,j}$, where $\sum\limits_{j=1}^{n_i}{p_{i,j}} = 1$. </p><p>Let's denote the amount of money assigned to $j$-th item of the topic $i$ as $c_{i, j}$; the total amount of money for the topic is $C_i = \sum\limits_{j=1}^{n_i}{c_{i,j}}$. A <span class="tex-font-style-it">non-optimality</span> of the plan for the topic $i$ is defined as $\sum\limits_{j=1}^{n_i}\left|\frac{c_{i, j}}{C_i} - p_{i, j}\right|$. Informally, the non-optimality is the total difference between the optimal and the actual ratios of money assigned to all the items in the topic. The <span class="tex-font-style-it">total plan non-optimality</span> is the sum of non-optimalities of all $t$ topics. Your task is to minimize the total plan non-optimality.</p><p>However, the exact amount of money available is not known yet. $j$-th item of $i$-th topic already has $\hat c_{i,j}$ dollars assigned to it and they cannot be taken back. Also, there are $q$ possible values of the extra unassigned amounts of money available $x_k$. For each of them, you need to calculate the minimal possible total non-optimality among all ways to distribute this extra money. You don't need to assign an integer amount of money to an item, any real number is possible, but all the extra money must be distributed among all the items in addition to $\hat c_{i,j}$ already assigned. Formally, for each value of extra money $x_k$ you'll need to find its distribution $d_{i,j}$ such that $d_{i, j} \ge 0$ and $\sum\limits_{i=1}^{t}\sum\limits_{j=1}^{n_i} d_{i,j} = x_k$, giving the resulting budget assignments $c_{i,j} = \hat c_{i,j} + d_{i,j}$ that minimize the total plan non-optimality.</p></div><div class="input-specification"><p>The first line contains two integers $t$ ($1 \le t \le 5 \cdot 10^4$) and $q$ ($1 \le q \le 3 \cdot 10^5$)&nbsp;— the number of topics in the budget and the number of possible amounts of extra money. </p><p>The next $t$ lines contain descriptions of topics. Each line starts with an integer $n_i$ ($2 \le n_i \le 5$)&nbsp;— the&nbsp;number of items in $i$-th topic; it is followed by $n_i$ integers $\hat c_{i, j}$ ($0 \le \hat c_{i, j} \le 10^5$; for any $i$, at least one of $\hat c_{i,j} &gt; 0$)&nbsp;— the&nbsp;amount of money already assigned to $j$-th item in $i$-th topic; they are followed by $n_i$&nbsp;integers $p'_{i,j}$ ($1 \le p'_{i,j} \le 1000$)&nbsp;— they determine the values of $p_{i,j}$ as $p_{i, j} = {p'_{i, j}} \big/ {\sum\limits_{j=1}^{n_i}{p'_{i, j}}}$ with $\sum\limits_{j=1}^{n_i}{p_{i,j}} = 1$. </p><p>The next line contains $q$ integers $x_k$ ($0 \le x_k \le 10^{12}$)&nbsp;— $k$-th possible amount of extra money. </p></div><div class="output-specification"><p>Output $q$ real numbers&nbsp;— the minimal possible non-optimality for the corresponding amount of extra money $x_k$. An absolute or a relative error of the answer must not exceed $10^{-6}$. </p></div>

## Input

<p>The first line contains two integers $t$ ($1 \le t \le 5 \cdot 10^4$) and $q$ ($1 \le q \le 3 \cdot 10^5$)&nbsp;— the number of topics in the budget and the number of possible amounts of extra money. </p><p>The next $t$ lines contain descriptions of topics. Each line starts with an integer $n_i$ ($2 \le n_i \le 5$)&nbsp;— the&nbsp;number of items in $i$-th topic; it is followed by $n_i$ integers $\hat c_{i, j}$ ($0 \le \hat c_{i, j} \le 10^5$; for any $i$, at least one of $\hat c_{i,j} &gt; 0$)&nbsp;— the&nbsp;amount of money already assigned to $j$-th item in $i$-th topic; they are followed by $n_i$&nbsp;integers $p'_{i,j}$ ($1 \le p'_{i,j} \le 1000$)&nbsp;— they determine the values of $p_{i,j}$ as $p_{i, j} = {p'_{i, j}} \big/ {\sum\limits_{j=1}^{n_i}{p'_{i, j}}}$ with $\sum\limits_{j=1}^{n_i}{p_{i,j}} = 1$. </p><p>The next line contains $q$ integers $x_k$ ($0 \le x_k \le 10^{12}$)&nbsp;— $k$-th possible amount of extra money. </p>

## Output

<p>Output $q$ real numbers&nbsp;— the minimal possible non-optimality for the corresponding amount of extra money $x_k$. An absolute or a relative error of the answer must not exceed $10^{-6}$. </p>





```input1
1 5
3 1 7 10 700 400 100
0 2 10 50 102
```




```input2
2 5
3 10 70 100 700 400 100
3 10 30 100 700 400 100
2 10 50 70 110
```




```output1
1.0555555555555556
0.8666666666666667
0.5476190476190478
0.12745098039215708
0.0
```




```output2
2.2967032967032974
2.216776340655188
1.8690167362600323
1.7301587301587305
1.5271317829457367
```


