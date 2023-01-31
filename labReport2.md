# CSE15L LabReport2
_Hello, today I will show how to setup a server StringServer, some JUnit tests, as well as share what things I learnt during Lab1 and Lab3!_
## Part1
For this part I have coded a server StringServer, which concatenates strings to each other, which are being inputted in the query of the server.
> The screenshot with the code that successfully implements the task and explanation for each line:

![Image1](ServerCode1.png)
- _line 11 checks if the path of the inputted URL contains `/add`; if **true**, then goes inside the if-statement; if **false**, returns `404 not found`
- _line 12 gets the string(query) after the `=` sign
- _lines 14 to 18 concatenate the inputted strings to each other
- _line 19 returns the result
