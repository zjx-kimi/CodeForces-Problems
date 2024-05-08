## Description

<div><p><span class="tex-font-style-bf">This is the medium version of the problem. The only difference between the three versions is the constraints on $n$ and $k$. You can make hacks only if all versions of the problem are solved.</span></p><p>Maxim is a minibus driver on Venus.</p><p>To ride on Maxim's minibus, you need a ticket. Each ticket has a number consisting of $n$ digits. However, as we know, the residents of Venus use a numeral system with base $k$, rather than the decimal system. Therefore, the ticket number can be considered as a sequence of $n$ integers from $0$ to $k-1$, inclusive.</p><p>The residents of Venus consider a ticket to be <span class="tex-font-style-it">lucky</span> if there is a digit on it that is equal to the sum of the remaining digits, modulo $k$. For example, if $k=10$, then the ticket $7135$ is lucky because $7 + 1 + 5 \equiv 3 \pmod{10}$. On the other hand, the ticket $7136$ is not lucky because no digit is equal to the sum of the others modulo $10$.</p><p>Once, while on a trip, Maxim wondered: how many lucky tickets exist? At the same time, Maxim understands that this number can be very large, so he is interested only in the answer modulo some prime number $m$.</p><center> <img class="tex-graphics" src="file://K3xgffO5.png" style="max-width: 100.0%;max-height: 100.0%;"> </center></div><div class="input-specification"><p>The only line of the input contains three integers $n$, $k$ and $m$ ($1 \le n \le 10^{18}$, $1 \le k \le 100$, $10^8 \le m \le 10^9 + 7$, $m$ is a prime number)&nbsp;— the number of digits on the ticket, the base of the numeral system on Venus, and the module for answer calculation.</p></div><div class="output-specification"><p>Print one integer&nbsp;— the number of lucky tickets modulo $m$, i.&nbsp;e. the remainder after dividing the answer by $m$.</p></div>

## Input

<p>The only line of the input contains three integers $n$, $k$ and $m$ ($1 \le n \le 10^{18}$, $1 \le k \le 100$, $10^8 \le m \le 10^9 + 7$, $m$ is a prime number)&nbsp;— the number of digits on the ticket, the base of the numeral system on Venus, and the module for answer calculation.</p>

## Output

<p>Print one integer&nbsp;— the number of lucky tickets modulo $m$, i.&nbsp;e. the remainder after dividing the answer by $m$.</p>





```input1
3 2 1000000007
```




```input2
3 4 1000000007
```




```output1
4
```




```output2
28
```



## Note

<p>In the first example, there are only four lucky tickets: $000$, $011$, $101$, and $110$.</p>
