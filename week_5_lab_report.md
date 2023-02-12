# 4 common find command-line options

find is a command that provides a powerful way to search for files and directories.
Today, we are going to closely examine 4 interesting command-line options for find.

## -name
- search for a file with a particular name

### -name Ex1
```
$ find -name Paris-WhereToGo.txt
./travel_guides/berlitz2/Paris-WhereToGo.txt
```
The command searches for the file with the name "Paris-WhereToGo.txt"

### -name Ex2
```
$ find non-fiction/OUP/Berk -name *.txt
non-fiction/OUP/Berk/CH4.txt
non-fiction/OUP/Berk/ch1.txt
non-fiction/OUP/Berk/ch2.txt
non-fiction/OUP/Berk/ch7.txt
```
The command searches for the file under the specific direcotry with the name of something plus ".txt"

source used: https://www.linuxteck.com/find-command-in-linux-with-examples/

## -iname
- search for files by approximate name(partial and case-insensitive search)

### -iname Ex1

```
$ find -iname bali-history.txt
./travel_guides/berlitz2/Bali-History.txt
```
The command searches for the file with the name "bali-history.txt" regardless of uppercase or lowercase

### -iname Ex2 
```
$ find -iname P*-wheretogo.txt
./travel_guides/berlitz2/Paris-WhereToGo.txt
./travel_guides/berlitz2/Portugal-WhereToGo.txt
./travel_guides/berlitz2/PuertoRico-WhereToGo.txt
```
The command searches for the file with the name beginning with the letter "P" and ending with "-wheretogo.txt" regardless of uppercase or lowercase

source used: https://www.redhat.com/sysadmin/linux-find-command

## -size
- search for files based on file size

### -size Ex1

```
$ find -size +200k
./travel_guides/berlitz1/WhereToFrance.txt
./travel_guides/berlitz1/WhereToItaly.txt
./travel_guides/berlitz2/Canada-WhereToGo.txt
```
The command searches for files with their sizes bigger than 200 KB

### -size Ex2 
```
$ find -size +10k -size -12k
./travel_guides/berlitz1/IntroFrance.txt
./travel_guides/berlitz1/IntroJamaica.txt
```
The command searches for files with their sizes between 10 and 12 KB

source used: https://linuxconfig.org/how-to-use-find-command-to-search-for-files-based-on-file-size

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
