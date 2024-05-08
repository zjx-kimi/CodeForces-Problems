## Description

<div><p>An expedition group flew from planet ACM-1 to Earth in order to study the bipedal species (its representatives don't even have antennas on their heads!).</p><p>The flying saucer, on which the brave pioneers set off, consists of three sections. These sections are connected by a chain: the 1-st section is adjacent only to the 2-nd one, the 2-nd one — to the 1-st and the 3-rd ones, the 3-rd one — only to the 2-nd one. The transitions are possible only between the adjacent sections.</p><p>The spacecraft team consists of <span class="tex-span"><i>n</i></span> aliens. Each of them is given a rank — an integer from <span class="tex-span">1</span> to <span class="tex-span"><i>n</i></span>. The ranks of all astronauts are distinct. The rules established on the Saucer, state that an alien may move from section <span class="tex-span"><i>a</i></span> to section <span class="tex-span"><i>b</i></span> only if it is senior in rank to all aliens who are in the segments <span class="tex-span"><i>a</i></span> and <span class="tex-span"><i>b</i></span> (besides, the segments <span class="tex-span"><i>a</i></span> and <span class="tex-span"><i>b</i></span> are of course required to be adjacent). Any alien requires exactly <span class="tex-span">1</span> minute to make a move. Besides, safety regulations require that no more than one alien moved at the same minute along the ship.</p><p>Alien <span class="tex-span"><i>A</i></span> is senior in rank to alien <span class="tex-span"><i>B</i></span>, if the number indicating rank <span class="tex-span"><i>A</i></span>, is more than the corresponding number for <span class="tex-span"><i>B</i></span>.</p><p>At the moment the whole saucer team is in the 3-rd segment. They all need to move to the 1-st segment. One member of the crew, the alien with the identification number CFR-140, decided to calculate the minimum time (in minutes) they will need to perform this task.</p><p>Help CFR-140, figure out the minimum time (in minutes) that all the astronauts will need to move from the 3-rd segment to the 1-st one. Since this number can be rather large, count it modulo <span class="tex-span"><i>m</i></span>.</p></div><div class="input-specification"><p>The first line contains two space-separated integers: <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> <span class="tex-span">(1 ≤ <i>n</i>, <i>m</i> ≤ 10<sup class="upper-index">9</sup>)</span> — the number of aliens on the saucer and the number, modulo which you should print the answer, correspondingly.</p></div><div class="output-specification"><p>Print a single number — the answer to the problem modulo <span class="tex-span"><i>m</i></span>.</p></div>

## Input

<p>The first line contains two space-separated integers: <span class="tex-span"><i>n</i></span> and <span class="tex-span"><i>m</i></span> <span class="tex-span">(1 ≤ <i>n</i>, <i>m</i> ≤ 10<sup class="upper-index">9</sup>)</span> — the number of aliens on the saucer and the number, modulo which you should print the answer, correspondingly.</p>

## Output

<p>Print a single number — the answer to the problem modulo <span class="tex-span"><i>m</i></span>.</p>





```input1
1 10

```




```input2
3 8

```




```output1
2

```




```output2
2

```



## Note

<p>In the first sample the only crew member moves from segment 3 to segment 2, and then from segment 2 to segment 1 without any problems. Thus, the whole moving will take two minutes.</p><p>To briefly describe the movements in the second sample we will use value <img align="middle" class="tex-formula" src="file://Jca1u5MO.png" style="max-width: 100.0%;max-height: 100.0%;">, which would correspond to an alien with rank <span class="tex-span"><i>i</i></span> moving from the segment in which it is at the moment, to the segment number <span class="tex-span"><i>j</i></span>. Using these values, we will describe the movements between the segments in the second sample: <img align="middle" class="tex-formula" src="file://oGSQVdb0.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://8UdHWF5T.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://jw9Zn8eC.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://EiRXgMFD.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://wktcSHzH.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://gVHChccR.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://LVX1i1zE.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://DpZWUgLo.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://p6YfgLRA.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://gbjrskvj.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://VJLvMufx.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://uxAuXFAx.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://i43nVCm3.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://zIhUlYCH.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://UcEzz67O.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://G0kbsfTC.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://RhO0dh4f.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://JtiXB2Ld.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://8jEuOUIf.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://rvygvtZJ.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://wGTGnTBo.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://PsEOeBQr.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://4dRDuaUx.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://Z2g9N1oZ.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://eqqZTLfP.png" style="max-width: 100.0%;max-height: 100.0%;">, <img align="middle" class="tex-formula" src="file://puUbOAJ9.png" style="max-width: 100.0%;max-height: 100.0%;">; In total: the aliens need 26 moves. The remainder after dividing <span class="tex-span">26</span> by <span class="tex-span">8</span> equals <span class="tex-span">2</span>, so the answer to this test is <span class="tex-span">2</span>.</p>
