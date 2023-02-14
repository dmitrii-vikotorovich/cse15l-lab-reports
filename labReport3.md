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
...and others
```
Or, for example, the pattern "Mountain" can be found in these files.
URL:(https://geekflare.com/grep-command-examples/)

## $ grep -n
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
...and others
```
We can use this command to search for a pattern in all text of a given directory. Example above.
URL:(https://geekflare.com/grep-command-examples/)

##
