## Description

<div><p>Dasha loves guinea pigs very much. In this regard, she decided to settle as many guinea pigs at home as possible and developed a plan for the next $n$ days. Every day, she will either buy a new guinea pig or call a doctor to examine all her pets.</p><p>Unfortunately, the store where she was going to buy guinea pigs does not understand them. Therefore, it cannot determine their gender. Dasha can't do it either. The only one who can help is a doctor. </p><p>To keep guinea pigs, aviaries are needed. Dasha plans to buy them in the same store. Unfortunately, only one species is sold there — a double aviary. No more than two guinea pigs can live in it.</p><p>Since Dasha does not want to cause moral injury to her pets — she will not settle two guinea pigs of different genders in one aviary.</p><p>Help Dasha calculate how many aviaries in the worst case you need to buy so that you can be sure that at no moment of time do two guinea pigs of different genders live in the same aviary.</p><p><span class="tex-font-style-bf">As part of this task, we believe that guinea pigs have only two genders — male and female.</span></p></div><div class="input-specification"><p>The first line of input data contains one number $t$ ($1 \leqslant t \leqslant 10^5$) — the number of input data sets.</p><p>The first line of each input data set contains one number $n$ ($1 \leqslant n \leqslant 10^5$) — the number of days Dasha has a plan for.</p><p>The next line contains $n$ numbers $b_1, b_2, b_3, \ldots, b_n$ ($1 \leqslant b_i \leqslant 2$) — Dasha's plan. If $b_i = 1$, then on the $i$th day, Dasha will buy a new guinea pig. If $b_i = 2$, then on the $i$th day, a doctor will come to Dasha and help determine the sex of all guinea pigs that Dasha already has.</p><p>It is guaranteed that the sum of $n$ for all input data sets does not exceed $10^5$.</p></div><div class="output-specification"><p>For each set of input data, output one number — the minimum number of aviaries Dasha needs to buy so that no matter what the genders of the pigs turn out to be, we can settle them so that at no point in time do two guinea pigs of different genders live together.</p></div>

## Input

<p>The first line of input data contains one number $t$ ($1 \leqslant t \leqslant 10^5$) — the number of input data sets.</p><p>The first line of each input data set contains one number $n$ ($1 \leqslant n \leqslant 10^5$) — the number of days Dasha has a plan for.</p><p>The next line contains $n$ numbers $b_1, b_2, b_3, \ldots, b_n$ ($1 \leqslant b_i \leqslant 2$) — Dasha's plan. If $b_i = 1$, then on the $i$th day, Dasha will buy a new guinea pig. If $b_i = 2$, then on the $i$th day, a doctor will come to Dasha and help determine the sex of all guinea pigs that Dasha already has.</p><p>It is guaranteed that the sum of $n$ for all input data sets does not exceed $10^5$.</p>

## Output

<p>For each set of input data, output one number — the minimum number of aviaries Dasha needs to buy so that no matter what the genders of the pigs turn out to be, we can settle them so that at no point in time do two guinea pigs of different genders live together.</p>





```input1|2,3,6,7,10,11
6
3
1 1 1
3
2 2 2
5
1 1 1 2 1
10
1 2 1 2 1 2 1 2 1 2
20
1 2 1 1 1 1 1 2 1 2 1 2 2 1 1 1 1 1 1 1
20
2 1 1 2 1 1 2 1 2 2 1 1 1 2 2 1 1 1 1 2
```




```output1
3
0
3
4
12
9
```



## Note

<p>In the first set of input data, Dasha needs to put each guinea pig in a separate enclosure, since she does not know their gender.</p><p>In the second set of input data, Dasha will buy $0$ guinea pigs, which means she will need $0$ aviaries.</p><p>In the third set of input data, you even need $3$ aviaries to put each guinea pig in a separate aviary before the doctor arrives at the $4$th day. When she finds out their gender, at least two guinea pigs will be of the same gender and they can be placed in one aviary, and the third in another aviary. Thus, she will have one free aviary in which she can settle a new guinea pig. So answer is $3$.</p><p>In the fourth set of input data, we show that $4$ is the optimal answer. </p><p>To begin with, we note that the first four guinea pigs can be placed one at a time in an aviary. Then a doctor will come and determine their gender. Among these four guinea pigs there will be at least one pair of the same gender, because: either male guinea pigs are at least $2$, or they are not more than $1$, which means that the female is at least $3$. Now we can put this couple in one aviary, and the other two in separate ones. We will have one more empty aviary where we can put a new pig.</p><p>Now let's show that the answer is at least $4$. Let's say that among the first $4$ guinea pigs, $3$ are female and $1$ is male. We need at least $3$ aviaries to settle them. Then, when we buy a new guinea pig, we will need another aviary in which we will put it, since we do not know its gender.</p>
