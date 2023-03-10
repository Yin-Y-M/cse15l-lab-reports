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
$ grep -i "wall" ./travel_guides/berlitz2/Beijing-History.txt  
The Ming rulers cautiously welcomed a few Catholic missionaries from Europe to Beijing. In the 17th century the Jesuits, headed by Matteo Ricci, had a profound influence not so much on Chinese religion (they made few converts among Beijingers) as on science, mathematics, astronomy, art, medicine, and other forms of knowledge that had never before been infused with Western ideas in China. Perhaps the greatest project of the Ming, however, was the restoration and extension of the Great Wall north of Beijing. For the first time, brick was used to finish these magnificent fortifications. It is the Ming Dynasty Great Wall that millions visit today at Beijing.
The Ming rulers were understandably nervous about yet another invasion from the north and took defensive measures by extending the Great Wall. They were nonetheless undone by precisely what they feared most: northern invaders. This time the conquerors were the Manchus, who established a dynasty that proved as long-lived and as glorious as the Ming.
The Chinese Communist party first initiated a popular program of reconstruction to transform and modernize the nation. In Beijing, the ancient city walls were pulled down and the city moat was filled in. Only a few of the venerable city gates and towers remain standing today. China’s first subway system now makes a loop that retraces the foundations of the city walls, with the subway stops named for the ancient city gates. Tiananmen Square was substantially enlarged, Chang’an Avenue widened, the Great Hall of the People built, the Museum of History and the Museum of the Revolution opened — all in the 1950s. Old neighborhoods began to be replaced by modern brick-and-concrete highrises. Beijing became its own powerful municipality (not part of any province), the seat of the new revolutionary government for the nation.
```
The command searches for the word "wall" in the file regardless of uppercase or lowercase.

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
- Display the matched lines and their line numbers.

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
The command searches for the string "Celtic" and we know that that this string was presented in line 7, 16, 20, 36, 43, 49 from the result.

### -n Ex2 
```
$ grep -n "1967" ./travel_guides/berlitz1/HistoryIsrael.txt
187:        Israel in 1967, the Israeli Air Force destroyed the air forces of
```
The command searches for the string "1967" and the result indicates that it was in line 187.

source used: https://www.geeksforgeeks.org/grep-command-in-unixlinux/

## -type
- search for files of a specific type

### -type Ex1

```
find -type d
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Berk
./non-fiction/OUP/Castro
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Rybczynski
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz2
```
The command searches for files of type d(directory)

### -type Ex2 
```
$ find non-fiction/OUP/Rybczynski -type f
non-fiction/OUP/Rybczynski/ch1.txt
non-fiction/OUP/Rybczynski/ch2.txt
non-fiction/OUP/Rybczynski/ch3.txt
```
The command searches for files of type f(regular file)

source used: https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/


other source used: ChatGPT
