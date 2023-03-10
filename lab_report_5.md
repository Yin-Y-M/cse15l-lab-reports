# 4 common grep command-line options



The grep command is a powerful tool for searching and manipulating text in Unix and Linux systems. 
In lab report 3, I have closely examined 4 commonand-line options for `find`.
Today, I will do the same for `grep`.

## -i
- Ignore uppercase vs. lowercase when matching text

### -i Ex1
```
$ grep -i "crete" ./travel_guides/berlitz1/HistoryGreek.txt

        Farther south in Crete, the Minoan culture developed after
        next major island north, was heavily influenced by Crete, and the
        whole Minoan civilization. Massive tidal waves swept over Crete, and
```
The command searches for the word "crete" in the file regardless of uppercase or lowercase.

### -i Ex2
```
$ grep -i "valley" ./travel_guides/berlitz1/HistoryEgypt.txt
        T he fertile Nile Valley has supported human life for over
        during this time. The Valley of the Kings was also chosen as a new
        entombed in a narrow valley across the river from the temple at
```
The command searches for the word "valley" in the file regardless of uppercase or lowercase.

source used: https://en.wikibooks.org/wiki/Grep

## -c
- Display the total number of times a string appears 

### -c Ex1

```
$ grep -c "Dynasty" ./travel_guides/berlitz2/China-History.txt
13
```
The command searches for the number of times the word "Dynasty" appears in the file.

### -c Ex2 
```
$ grep -c "British" ./travel_guides/berlitz2/Canada-History.txt
27
```
The command searches for the number of times the word "British" appears in the file.

source used:  https://allthings.how/how-to-use-grep-command-in-linux/

## -n
- Display the matched lines and their line numbers

### -n Ex1

```
$ grep -n "Celtic" ./travel_guides/berlitz1/HistoryDublin.txt
7:        Celtic Ireland
16:        system, and Celtic Ireland became a series of independent kingdoms.
20:        the poet was held in awe. Law and religion were important in Celtic
36:        With Christianity and the sophisticated Celtic culture
43:        cannot be overrated. However, the Irish church with its Celtic cultural
49:        continued much as it had under pagan Celtic rule. There were still no
```
The command searches for the lines containing the string "Celtic" and display the line number in the front.

### -n Ex2 
```
$ grep -n "1967" ./travel_guides/berlitz1/HistoryIsrael.txt
187:        Israel in 1967, the Israeli Air Force destroyed the air forces of
```
The command searches for the lines containing the string "1967" and display the line number in the front.

source used: https://www.geeksforgeeks.org/grep-command-in-unixlinux/

## -l
- Display only the file names which matches the given pattern using

### -l Ex1

```
$ grep -l "U.S." ./travel_guides/berlitz1/*.txt
./travel_guides/berlitz1/HandRIsrael.txt
./travel_guides/berlitz1/HandRMadrid.txt
./travel_guides/berlitz1/WhatToHawaii.txt
./travel_guides/berlitz1/WhatToIbiza.txt
./travel_guides/berlitz1/WhatToIsrael.txt
./travel_guides/berlitz1/WhereToHawaii.txt
./travel_guides/berlitz1/WhereToIndia.txt
./travel_guides/berlitz1/WhereToLosAngeles.txt
```
The command searches for files in the target directory containing the string "U.S."

### -l Ex2 
```
$ grep -l "Canada" ./travel_guides/berlitz2/*.txt
./travel_guides/berlitz2/Bermuda-history.txt
./travel_guides/berlitz2/California-WhatToDo.txt
./travel_guides/berlitz2/Canada-History.txt
./travel_guides/berlitz2/Canada-WhereToGo.txt
./travel_guides/berlitz2/NewOrleans-History.txt
```
The command searches for files in the target directory containing the string "Canada."

source used: https://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/


other source used: ChatGPT
