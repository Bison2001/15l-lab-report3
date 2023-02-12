# Grep

## -i

### Example 1
```
Command: $ grep -i "ITALY" travel_guides/berlitz1/WhereToItaly.txt`
Output:
        decisions. “ Doing” Italy is a lifetime job, and many devotees are so
        principal city as a focus or starting point: Rome for central Italy,
        Given the sheer and unrivaled richness of Italy, the
        ...
```
### Example 2
```
Command: $ grep -i "italy" travel_guides/berlitz1/WhereToItaly.txt`
Output:
        decisions. “ Doing” Italy is a lifetime job, and many devotees are so
        principal city as a focus or starting point: Rome for central Italy,
        Given the sheer and unrivaled richness of Italy, the
        ...
```
### Summary
We are trying to find all the lines in the file "WhereToItaly.txt" that contains the word "Italy". The `-i` option allows us to find any word that is "Italy" without worrying about lowercase or uppercse. This is useful since we don't need to consider whether the word "Italy" appears as "ITALY" or "italy" in the text files.

### Source
https://www.geeksforgeeks.org/grep-command-in-unixlinux/

## -c

### Example 1
```
Command: $ grep -c "Italy" travel_guides/berlitz1/WhereToItaly.txt`
Output: 78
```

### Example 2
```
Command: $ grep -c "ITALY" travel_guides/berlitz1/WhereToItaly.txt`
Output: 1
```

### Summary
We are trying to count how many lines in the file "WhereToItaly.txt" that contains the word "Italy" or "ITALY". `-c` command allow us to count the number of lines that contain a given string in some files. The first example count the word "Italy" and the second count "ITALY". This command allow us to examine word frequency in a given txt.

### Source
https://www.geeksforgeeks.org/grep-command-in-unixlinux/

## -l

### Example 1
```
Command: $ grep -l "Italy" travel_guides/berlitz1/*
Output:
      travel_guides/berlitz1/HistoryFrance.txt
      travel_guides/berlitz1/HistoryGreek.txt
      travel_guides/berlitz1/HistoryIstanbul.txt
      travel_guides/berlitz1/HistoryItaly.txt
      travel_guides/berlitz1/HistoryMadeira.txt
      travel_guides/berlitz1/HistoryMallorca.txt
      travel_guides/berlitz1/IntroItaly.txt
      travel_guides/berlitz1/IntroLasVegas.txt
      travel_guides/berlitz1/WhatToItaly.txt
      travel_guides/berlitz1/WhereToEgypt.txt
      travel_guides/berlitz1/WhereToFWI.txt
      travel_guides/berlitz1/WhereToFrance.txt
      travel_guides/berlitz1/WhereToGreek.txt
      travel_guides/berlitz1/WhereToIstanbul.txt
      travel_guides/berlitz1/WhereToItaly.txt
      travel_guides/berlitz1/WhereToMadrid.txt
```

### Example 2
```
Command: $ grep -l "Ravenna" travel_guides/berlitz1/*
Output:
      travel_guides/berlitz1/HistoryItaly.txt
      travel_guides/berlitz1/IntroItaly.txt
      travel_guides/berlitz1/WhatToItaly.txt
      travel_guides/berlitz1/WhereToItaly.txt
```

### Summary
We are trying to find all files in the `travel_guides/berlitz1` directory that contains the word " Italy" in Example 1 or "Ravenna" in Example 2. `-l` option allows us to return the file name of the file that contains the given String. This is useful when we are only interested in the file name.

### Source
https://www.geeksforgeeks.org/grep-command-in-unixlinux/

## -w

### Example 1
```
Command: $ grep -w "Rome" travel_guides/berlitz1/WhereToItaly.txt`
Output:
        destination. After a predictable first romance with Rome, Venice, or
        principal city as a focus or starting point: Rome for central Italy,
        the regions. Those with a passion for the big city can combine Rome
        ...
```

### Example 2
```
Command: $ grep -w "Pantheon" travel_guides/berlitz1/WhereToItaly.txt`
Output:
        The circular Pantheon (Piazza della Rotonda) is the
        cast out of bronze beams taken from the Pantheon’s porch (see page 51),
```

### Summary
We are trying to find all the lines in "WhereToItaly.txt" that contain the whole word "Rome". So, if the word "Rome" appears as a substring like "Romance", it cannot be matched. The `-w` option allows us to match the whole word. It is useful when we only want to find the whole word instead of finding a substring.

### Source
https://www.geeksforgeeks.org/grep-command-in-unixlinux/
