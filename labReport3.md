# CSE15L LabReport3
Hello, today I will work with the `grep` command. I will show you 4 variations and alternate ways to use this command. For each of them I will provide to examples of using it on our **./written_2** directory. Let's begin!
##  grep -r -l
An alternative way to find the file that contains the string "Lucayans" in the data directory is to use `grep -r -l "Lucayans"`.
```
$  grep -r -l "Lucayans"
written_2/travel_guides/berlitz2/Bahamas-History.txt
```
Basically, `grep`command-line tool is used to search for regular expressions. Here, I also added `-r` and `-l` flags to search for "Lucayans". The `-r` flag is used to look through all of the subdirectories to find a specific pattern. The `-l` flag is used to print the names of the files where the pattern (in our case "Lucayans") is found. Combining them, returns the path to all files where the string "Lucayans" is. (in our case it's **written_2/travel_guides/berlitz2/Bahamas-History.txt**).
```
$  grep -r -l "Mountain"
written_2/travel_guides/berlitz1/HandRJamaica.txt
written_2/travel_guides/berlitz1/IntroDublin.txt
written_2/travel_guides/berlitz1/WhatToIndia.txt
written_2/travel_guides/berlitz1/WhatToIsrael.txt
written_2/travel_guides/berlitz1/WhatToIstanbul.txt
```
Or, for example, the pattern "Mountain" can be found in these files.
URL:(https://geekflare.com/grep-command-examples/)

## grep -n
```
$ grep -n "Mountain" written_2/travel_guides/berlitz1/WhatToIsrael.txt
112:        hiking in the Eilat Mountains Reserve and in the Sinai.
```
This grep command with the `-n` flag not only finds the occurence of a pattern in a given file, but also prints the line where this pattern is.
```
$ grep -n "Volcano" written_2/travel_guides/berlitz1/*.txt
written_2/travel_guides/berlitz1/HandRHawaii.txt:142:        Chalet Kilauea $$–$$$ P.O. Box 998, Volcano, HI 96785; Tel.
written_2/travel_guides/berlitz1/HandRHawaii.txt:145:        of bed & breakfast accommodations in the Volcano area. They have
written_2/travel_guides/berlitz1/IntroFWI.txt:19:        steep hills and rolling plains. Volcanoes, hummingbirds, mangroves,
written_2/travel_guides/berlitz1/WhereToFWI.txt:333:        Vacillating Volcano
```
We can use this command to search for a pattern in all text of a given directory. Example above.
URL:(https://geekflare.com/grep-command-examples/)

## grep -w
```
$ grep -w "Russia" written_2/travel_guides/berlitz1/*.txt
written_2/travel_guides/berlitz1/HistoryFrance.txt:        During his disastrous campaign in Russia, he found time in Moscow to
written_2/travel_guides/berlitz1/HistoryFrance.txt:        Europe’s Ancien Régime turned against him in Spain, Russia, and
written_2/travel_guides/berlitz1/HistoryGreek.txt:        Russia came to aid the Greeks (defined by their Orthodox religion
written_2/travel_guides/berlitz1/HistoryIndia.txt:        Originally from Russia or Asia, they migrated to Mesopotamia first and
```
This grep command variation with a `-w` flag finds the actual pattern (in our case "Russia") instead of finding also the modifications of this word. For example, the `$ grep -n "Volcano" written_2/travel_guides/berlitz1/*.txt` command would print lines that contain words **Russian** or **Russians** as well.
```
$ grep -r -l -w "Russia" written_2/travel_guides/berlitz1/*.txt
written_2/travel_guides/berlitz1/HistoryFrance.txt
written_2/travel_guides/berlitz1/HistoryGreek.txt
written_2/travel_guides/berlitz1/HistoryIndia.txt
written_2/travel_guides/berlitz1/HistoryItaly.txt
```
The flags `-r`,`-l`,`-w` and many others can be combined. For example, in this case the output is the paths to all **.txt** files in all the subdirectories that contain the pattern "Russia" and only "Russia".
URL:(https://geekflare.com/grep-command-examples/)

## grep -c
```
$ grep -c  "San Diego" written_2/travel_guides/berlitz1/*.txt
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:3
written_2/travel_guides/berlitz1/WhereToMadeira.txt:0
written_2/travel_guides/berlitz1/WhereToMadrid.txt:0
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:0
```
Here, the `-c` flag prints how many occurences of a pattern (in our case "San Diego") is in all **.txt** files in this directory **written_2/travel_guides/berlitz1/** and the paths to the files. As we can see, only the travel guide to Los Angeles has occurences of "San Diego", while travel guides to the country Malaysia or a spanish capital Madrid have no mentions of "San Diego", which makes total sense.
```
$ grep -r -c "Code" written_2/travel_guides/berlitz2/*.txt
written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt:0
written_2/travel_guides/berlitz2/NewOrleans-History.txt:1
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt:1
```
Here, we are trying to find the pattern "Code" in all **.txt** files in this directory **written_2/travel_guides/berlitz2/**. As we can see there is 1 occurence of "Code" in the travel guide to New Orleans and in the travel guide to Paris, which makes sense,because, as is widely known, the best programmers come from New Orleans.
URL:(https://geekflare.com/grep-command-examples/)

## Conclusion
This is all I wanted to show regarding different variations and tricks with the `grep` command-line tool.
