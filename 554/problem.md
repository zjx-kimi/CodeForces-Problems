## Description

<div><p>During the latest mission of the starship U.S.S. Coder, Captain Jan Bitovsky was accidentally teleported to the surface of an unknown planet. </p><p>Trying to find his way back, Jan found an artifact from planet Earth's ancient civilization — a mobile device capable of interstellar calls created by Byterola. Unfortunately, there was another problem. Even though Jan, as a representative of humans, knew perfectly the old notation of the cell phone numbers, the symbols on the device's keyboard were completely worn down and invisible to the human eye. The old keyboards had exactly $m + 1$ buttons, one for each digit from the base $m$ numerical system, and one single backspace button allowing one to erase the last written digit (if nothing was written on the screen, then this button does nothing, but it's still counted as pressed).</p><p>Jan would like to communicate with his crew. He needs to type a certain number (also from the base $m$ numerical system, that is, digits from $0$ to $m - 1$). He wants to know the expected number of button presses necessary to contact the U.S.S. Coder. Jan always chooses the most optimal buttons based on his current knowledge. Buttons are indistinguishable until pressed. Help him!</p></div><div class="input-specification"><p>In the first line of input, there are two integer numbers $n$ and $m$ ($1 \le n \le 10^6$, $2 \le m \le 10^3$) — the length of the number to U.S.S. Coder and the base of the numerical system.</p><p>In the next and the last input line, there are $n$ integers between $0$ and $m - 1$: the number to type in the base $m$ numerical system.</p></div><div class="output-specification"><p>Output the expected number of button presses modulo $1\,000\,000\,007$.</p><p>Formally, let $M = 1\,000\,000\,007$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0 \pmod{M}$. Output the integer equal to $p \cdot q^{-1} \bmod M$. In other words, output such an integer $x$ that $0 \le x &lt; M$ and $x \cdot q \equiv p \pmod{M}$.</p></div>

## Input

<p>In the first line of input, there are two integer numbers $n$ and $m$ ($1 \le n \le 10^6$, $2 \le m \le 10^3$) — the length of the number to U.S.S. Coder and the base of the numerical system.</p><p>In the next and the last input line, there are $n$ integers between $0$ and $m - 1$: the number to type in the base $m$ numerical system.</p>

## Output

<p>Output the expected number of button presses modulo $1\,000\,000\,007$.</p><p>Formally, let $M = 1\,000\,000\,007$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0 \pmod{M}$. Output the integer equal to $p \cdot q^{-1} \bmod M$. In other words, output such an integer $x$ that $0 \le x &lt; M$ and $x \cdot q \equiv p \pmod{M}$.</p>





```input1
1 2
0
```




```input2
2 3
0 0
```




```input3
2 3
0 1
```




```output1
666666674
```




```output2
916666678
```




```output3
500000009
```



## Note

<p>In the first example, two digits ($0$ and $1$) and a backspace button are available on the keyboard. Jan has no way of knowing which one is which, so he presses a random one. </p><p>With probability $\frac{1}{3}$, he presses $0$ and manages to type the crew's number. </p><p>With probability $\frac{1}{3}$, he presses backspace, and nothing happens. Then with probability $\frac{1}{2}$ he manages to press $0$ (finishing the process). Otherwise, with probability $\frac{1}{2}$, he types $1$, which he then needs to remove with backspace and hit the last button, which has to be $0$. In this case, he needs $4$ button presses.</p><p>At last, he might press the $1$ button first, also with probability $\frac{1}{3}$. Then, if he presses the backspace with a chance of $50\%$, he is all set and only needs to press the last button (3 presses in total). In the worst case, he would press the $0$ button first and need to remove both with backspace, then finally type the number $0$ (5 presses in total).</p><p>We get the expected value of $\frac{16}{6}$. The modular inverse of $6$ modulo $1\;000\;000\;007$ is $166666668$, so $16 \cdot 166666668 = 666666674 \mod \; 1\;000\;000\;007$</p>
