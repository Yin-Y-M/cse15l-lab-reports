# 4 common find command-line options

find is a command that provides a powerful way to search for files and directories.
Today, we are going to closely examine 4 interesting command-line options for find.

## -name
Ignore uppercase vs. lowercase.

### -name Ex1
When 
```
$ find -name Paris-WhereToGo.txt
./travel_guides/berlitz2/Paris-WhereToGo.txt
```

### -name Ex2
```
$ find non-fiction/OUP/Berk -name *.txt
non-fiction/OUP/Berk/CH4.txt
non-fiction/OUP/Berk/ch1.txt
non-fiction/OUP/Berk/ch2.txt
non-fiction/OUP/Berk/ch7.txt
```

source used: https://en.wikibooks.org/wiki/Grep



## -size

### -size Ex1

```
$ find -size +200k
./travel_guides/berlitz1/WhereToFrance.txt
./travel_guides/berlitz1/WhereToItaly.txt
./travel_guides/berlitz2/Canada-WhereToGo.txt
```

### -size Ex2 
```
find -size -2k
./travel_guides/berlitz1/HandRIbiza.txt
./travel_guides/berlitz1/HandRIstanbul.txt
```
