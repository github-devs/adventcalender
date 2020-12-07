# adventcalender


This branch contains the trainer notes and different results for each step in the workshop. The files are stored in the notes directory in seperate directories.

We are building an advent calender in 7 steps. Each day in December, a new popular quote is availalbe in our advent calender.

There is an main branch with some examples, which should not be changed anymore. There is a `release/2020` which should contain all our current changes. This branch will be used for test and for production.

Our default workflow is 
* create a feature branch from `release/2020`
* apply the changes as described in the user stories
* commit your changes with a comment in the following format "US-NN: 'and some comment'", where USNN is your current user story.
* push your branch to the remote repository on GitHub
* create a pull request (PR)
* find a collegue to approve your PR
* merge the PR into `release/2020` and delete the feature branch


## step 0
As a trainer prepare the repository. You will find some dummy files and the README in the `main` branch. Create the `release/2020` branch on the command line and push it to the repo.

```
git checkout -b release/2020
git push -u origin release/2020
```

Then add restriction rules to all branches matching `release/*`.

## step 1
The participants should build the first set of cards for the advent calender. For each day a seperate file is created. The naming convention for cards is: "ordinalnumber_day.txt" i.e. 1st_day.txt, 2nd_day.txt, ...

The file contains 3 lines:
- day
- quote
- author

```
1
I'm not a great programmer. I'm just a good programmer with great habits.
Kent Beck
```

## step 2
The trainer changes all files to a new format, so there is merge conflict when the participants commit their next changes. The files are stored in the `notes/step2` folder.

```
git checkout trainer_notes
mkdir ../temp
cp notes/step2/* ../temp
git checkout release/2020
git pull
cp ../temp/* .
./git_actions
```

Then create a PR and merge it into `release/2020`. 

**Wait unitl the participants started their tasks!**

## step 3
The participants receive a new user story. In this story the need to adapt the current content to a new format.

```
1st
I'm not a great programmer. I'm just a good programmer with great habits.
Kent Beck
```

Due to step3 they will face a merge conflict when merging their PR.

## step 4
After merging their files the content should look like this example.

```
1st Dec
I'm not a great programmer. I'm just a good programmer with great habits.
Kent Beck
```

## step 5
We have released `release/2020` to production. We start with the development of the advent calender 2021. Therefore a new branch `release/2021` is created. In 2021 we want to privide different type of quotes in the calender. We have multiple directories for each type. The current quote are moved to a `software` directory. The participants will create new entries with general quotes and store them in a seperate `life` folder.

```
git checkout release/2020
git pull
git checkout -b release/2021
git push -u origin release/2021

git checkout -b new_release
mkdir software
mv *.txt software
git add *
git commit -m "new folder structure for 2021"
```

## step 6
We need a hotfix in production. During an update of the application the format was changed to YAML. 
```
day: 1st Dec
quote: I'm not a great programmer. I'm just a good programmer with great habits.
author: Kent Beck
```

The corrected files are stored in the `notes/step6` folder.
```
git checkout trainer_notes
mkdir ../temp
cp notes/step6/* ../temp
git checkout release/2020
git pull
cp ../temp/* .
./git_actions
```

## step 7
We need another hotfix in production. There is a bug rendering the current year. We need to add the current year to the day line.
```
day: 1st Dec 2020
quote: I'm not a great programmer. I'm just a good programmer with great habits.
author: Kent Beck
```

The corrected files are stored in the `notes/step7` folder.
```
git checkout trainer_notes
mkdir ../temp
cp notes/step7/* ../temp
git checkout release/2020
git pull
cp ../temp/* .
./git_actions
```

## step8 
The participants need to change all files to the YAML format in the `release/2021` branch. The changes should be cherry-picked from the `release/2020` branch.

Ask the participant, why we are not able to merge the changes?
