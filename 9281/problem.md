## Description

<div><p>So, the New Year holidays are over. Santa Claus and his colleagues can take a rest and have guests at last. When two "New Year and Christmas Men" meet, thear assistants cut out of cardboard the letters from the guest's name and the host's name in honor of this event. Then the hung the letters above the main entrance. One night, when everyone went to bed, someone took all the letters of our characters' names. Then he may have shuffled the letters and put them in one pile in front of the door.</p><p>The next morning it was impossible to find the culprit who had made the disorder. But everybody wondered whether it is possible to restore the names of the host and his guests from the letters lying at the door? That is, we need to verify that there are no extra letters, and that nobody will need to cut more letters.</p><p>Help the "New Year and Christmas Men" and their friends to cope with this problem. You are given both inscriptions that hung over the front door the previous night, and a pile of letters that were found at the front door next morning.</p></div><div class="input-specification"><p>The input file consists of three lines: the first line contains the guest's name, the second line contains the name of the residence host and the third line contains letters in a pile that were found at the door in the morning. All lines are not empty and contain only uppercase Latin letters. The length of each line does not exceed <span class="tex-span">100</span>.</p></div><div class="output-specification"><p>Print "<span class="tex-font-style-tt">YES</span>" without the quotes, if the letters in the pile could be permuted to make the names of the "New Year and Christmas Men". Otherwise, print "<span class="tex-font-style-tt">NO</span>" without the quotes.</p></div>

## Input

<p>The input file consists of three lines: the first line contains the guest's name, the second line contains the name of the residence host and the third line contains letters in a pile that were found at the door in the morning. All lines are not empty and contain only uppercase Latin letters. The length of each line does not exceed <span class="tex-span">100</span>.</p>

## Output

<p>Print "<span class="tex-font-style-tt">YES</span>" without the quotes, if the letters in the pile could be permuted to make the names of the "New Year and Christmas Men". Otherwise, print "<span class="tex-font-style-tt">NO</span>" without the quotes.</p>





```input1
SANTACLAUS
DEDMOROZ
SANTAMOROZDEDCLAUS

```




```input2
PAPAINOEL
JOULUPUKKI
JOULNAPAOILELUPUKKI

```




```input3
BABBONATALE
FATHERCHRISTMAS
BABCHRISTMASBONATALLEFATHER

```




```output1
YES

```




```output2
NO

```




```output3
NO

```



## Note

<p>In the first sample the letters written in the last line can be used to write the names and there won't be any extra letters left.</p><p>In the second sample letter "<span class="tex-font-style-tt">P</span>" is missing from the pile and there's an extra letter "<span class="tex-font-style-tt">L</span>".</p><p>In the third sample there's an extra letter "<span class="tex-font-style-tt">L</span>".</p>
