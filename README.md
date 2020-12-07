# adventcalender


This branch contains the trainer notes and different results for each step in the workshop. The files are stored in the notes directory in seperate directories.

We are building an advent calender in 7 steps. Each day in December, a new popular quote is availalbe in our advent calender.

There is an main branch with some examples, which should not be changed anymore. There is a release/2020 which should contain all our current changes. This branch will be used for test and for production.

Our default workflow is 
* create a feature branch from release/2020
* apply the changes as described in the user stories
* commit your changes with a comment in the following format "US-NN: 'and some comment'", where USNN is your current user story.
* push your branch to the remote repository on GitHub
* create a pull request (PR)
* find a collegue to approve your PR
* merge the PR into release/2020 and delete the feature branch

## step 1
The participants should build the first set of cards for the advent calender. For each day a seperate file is created. The naming convention for cards is: "ordinalnumber_day.txt" i.e. 1st_day.txt, 2nd_day.txt, ...

The file contains 3 lines:
- day
- quote
- author

## example 1st_day.txt
```
1
I'm not a great programmer. I'm just a good programmer with great habits.
Kent Beck
```
