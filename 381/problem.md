## Description

<div><p>There is a building named Taman Membeku (shortened as Tamem). The building has $N$ floors numbered from $1$ to $N$ from bottom to top. The only way to move between floors in the building is to use elevators. There are $3$ elevators available in Tamem, namely elevators $1$, $2$, and $3$.</p><p>Pak Chanek works as an elevator operator in Tamem. Pak Chanek will work for $Q$ days. Initially, each elevator is in floor $1$ and all elevators are on. On each day, exactly one of the following will happen: </p><ul> <li> <span class="tex-font-style-tt">1 x y</span> – There is a person currently in floor $x$ who wants to go to floor $y$. ($1\leq x,y\leq N$; $x\neq y$) </li><li> <span class="tex-font-style-tt">2 p</span> – Elevator $p$ changes state <span class="tex-font-style-bf">at the start of the day</span>. If previously it is on, then it will turn off. If previously it is off, then it will turn on. ($1\leq p\leq3$) </li></ul><p>For each day, Pak Chanek can control the movement of all elevators as he pleases. However, for each day where there is a person currently in floor $x$ who wants to go to floor $y$, among all elevator movements done by Pak Chanek, the following must happen: </p><ol> <li> One elevator moves to floor $x$. </li><li> The person gets into the elevator. </li><li> The elevator moves to floor $y$. </li><li> The person gets out of the elevator. </li></ol><p>For each day, Pak Chanek can only move the elevators that are currently on. Note that, since a change in state happens at the start of the day, this means that an elevator that turns off on some day starts becoming unusable from that day itself. Conversely, an elevator that turns on on some day starts becoming usable from that day itself.</p><p>It is known that the electricity fee for each day is different. More specifically, on the $j$-th day, the fee needed to move one elevator up or down by one floor is $A_j$.</p><p>From the start, Pak Chanek already knows the electricity fees and the sequence of events that will happen on the $Q$ days, so Pak Chanek can operate the elevators strategically. What is the minimum possible electricity fee to fulfill all needs of the people who want to move between floors in Tamem? Note: in the end, each elevator does not have to go back to floor $1$.</p></div><div class="input-specification"><p>The first line contains two integers $N$ and $Q$ ($2\leq N\leq10^5$; $1\leq Q\leq300$) — the number of floors and the number of days.</p><p>The second line contains $Q$ integers $A_1, A_2, A_3 \ldots, A_Q$ ($1 \leq A_j \leq 10^5$) — the electricity fee for each day.</p><p>The $j$-th of the next $Q$ lines contains the $j$-th event as described. At any moment, there will always be at least one elevator that is on.</p></div><div class="output-specification"><p>An integer representing the minimum possible electricity fee to fulfill all needs of the people who want to move between floors in Tamem.</p></div>

## Input

<p>The first line contains two integers $N$ and $Q$ ($2\leq N\leq10^5$; $1\leq Q\leq300$) — the number of floors and the number of days.</p><p>The second line contains $Q$ integers $A_1, A_2, A_3 \ldots, A_Q$ ($1 \leq A_j \leq 10^5$) — the electricity fee for each day.</p><p>The $j$-th of the next $Q$ lines contains the $j$-th event as described. At any moment, there will always be at least one elevator that is on.</p>

## Output

<p>An integer representing the minimum possible electricity fee to fulfill all needs of the people who want to move between floors in Tamem.</p>





```input1
9 8
3 4 4 3 4 2 7 6
1 2 7
1 3 9
2 2
1 4 5
1 3 5
2 2
1 7 3
1 2 1
```




```output1
114
```



## Note

<p>The following is an example of an optimal strategy: </p><ol> <li> On the $1$-st day: <ul> <li> Elevator $2$ moves to floor $3$. </li><li> Elevator $3$ moves to floor $2$, picks the person up, moves to floor $7$, then drops the person off. </li></ul> </li><li> On the $2$-nd day: <ul> <li> Elevator $2$ picks the person up, moves to floor $9$, then drops the person off. </li></ul> </li><li> On the $3$-rd day: <ul> <li> Elevator $2$ turns off. </li></ul> </li><li> On the $4$-th day: <ul> <li> Elevator $3$ moves to floor $4$, picks the person up, moves to floor $5$, drops the person off, then moves to floor $3$. </li></ul> </li><li> On the $5$-th day: <ul> <li> Elevator $3$ picks the person up, moves to floor $5$, then drops the person off. </li></ul> </li><li> On the $6$-th day: <ul> <li> Elevator $2$ turns on. </li><li> Elevator $1$ moves to floor $2$. </li><li> Elevator $2$ moves to floor $7$. </li></ul> </li><li> On the $7$-th day: <ul> <li> Elevator $2$ picks the person up, moves to floor $3$, then drops the person off. </li></ul> </li><li> On the $8$-th day: <ul> <li> Elevator $1$ picks the person up, moves to floor $1$, then drops the person off. </li></ul> </li></ol><p>The total electricity fee for each day from the $1$-st day to the $8$-th day are $24$, $24$, $0$, $18$, $8$, $6$, $28$, and $6$ respectively. Therefore, the total electricity fee for the entire $Q$ days is $24+24+0+18+8+6+28+6=114$.</p><p>It can be obtained that there is no strategy that requires a smaller electricity fee.</p>
