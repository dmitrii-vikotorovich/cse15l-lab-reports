# CSE15L Lab Report 5
***
The lab activity that I liked the most definetely was testing out various bash commands. In my **Lab Report 3** I researched `<grep>` and `<find>` commands; however, in this **Lab Report 5** I plan to cover more interesting and useful bash commands. Let's begin!
***
## rm
One can use the `<rm>` command to remove files or directories. But one of the issues with it, is that you have to be very careful when using to delete files or directories for the most part, because it's nearly impossible to gain access to the removed files back. The code snippet below is one example pf using this command.
```
$ ls
'Screenshot (10).png'  'Screenshot (30).png'  'Screenshot (53).png'
'Screenshot (11).png'  'Screenshot (31).png'  'Screenshot (54).png'
$ touch hello.png
$ ls
'Screenshot (10).png'  'Screenshot (30).png'  'Screenshot (53).png'
'Screenshot (11).png'  'Screenshot (31).png'  'Screenshot (54).png'
'hello.png'
$ rm hello.png
$ ls
'Screenshot (10).png'  'Screenshot (30).png'  'Screenshot (53).png'
'Screenshot (11).png'  'Screenshot (31).png'  'Screenshot (54).png'
```
If one wants to delete an empty directory the recursive (-r) flag could be used:

