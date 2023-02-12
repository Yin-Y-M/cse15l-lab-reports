# 4 common find command-line options

find is a command that provides a powerful way to search for files and directories.
Today, we are going to closely examine 4 interesting command-line options for find.

## -name
- search a file with a particular name

### -name Ex1
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

source used: https://www.linuxteck.com/find-command-in-linux-with-examples/

## -iname
- search files by approximate name(partial and case-insensitive search)

### -iname Ex1

```
$ find -iname bali-history.txt
./travel_guides/berlitz2/Bali-History.txt
```

### -iname Ex2 
```
$ find -iname P*-wheretogo.txt
./travel_guides/berlitz2/Paris-WhereToGo.txt
./travel_guides/berlitz2/Portugal-WhereToGo.txt
./travel_guides/berlitz2/PuertoRico-WhereToGo.txt
```

source used: https://www.redhat.com/sysadmin/linux-find-command

## -size
- search files based on file size

### -size Ex1

```
$ find -size +200k
./travel_guides/berlitz1/WhereToFrance.txt
./travel_guides/berlitz1/WhereToItaly.txt
./travel_guides/berlitz2/Canada-WhereToGo.txt
```

### -size Ex2 
```
$ find -size +10k -size -12k
./travel_guides/berlitz1/IntroFrance.txt
./travel_guides/berlitz1/IntroJamaica.txt
```

source used: https://linuxconfig.org/how-to-use-find-command-to-search-for-files-based-on-file-size

other source used: ChatGPT
