# Adventcalender Git Dojo


![Image logo](./adventcalender.jpg)

We are building an advent calender in multiple steps. Each day in December, a new popular quote is availalbe in our advent calender.

There is the `main` branch, which should not be changed anymore. There is a `releases/2020` branch, which should contain all our current changes. This branch will be used for test and for production.

After setting up your local environment the default workflow is 
* Create a local feature branch from `releases/2020` and call it according to your naming conventions `[USERID]/[TICKETID]/2020`
* Apply the changes as described in the user stories
* Commit your changes with a comment in the following the Azp naming conventions `[TICKETID] and some comment` 
* Push your local branch to the remote repository on GitHub
* Create a pull request (PR) in GitHub
* Find a collegue to approve your PR and assign it
* Merge and squash the PR into `releases/2020`
* Delete the feature branch

[See her for detailed list of commands](./workflows.md)

## Prerequisites and Setup
* Setup your Git User (register if necessary)
* Send the trainer your user-id, so you can be added to the group
* Check your access and try to login to [https://github.com/github-devs/adventcalender](https://github.com/github-devs/adventcalender)
* Check your git installation locally: open a GitBash and execute 
```
git --version
```
* Optional: An IDE like Eclipse is installed
* Navigate to a root folder for the exercise
* Clone the training repository locally: 
```
git clone https://github.com/github-devs/adventcalender.git
```
* Change your directory in your bash: 
```
cd adventcalender
```

* Switch to branch `releases/2020`: 
```
git checkout releases/2020
```


## Instructions Task 1: creating the calendar entries

December is coming soon. We have to deliver our first version of the calender asap. The trainer will create multiple teams and you will be assigned to one of them. Together with your team you should fullfill your task to create a calendar entry ([look here how to create it](tasks1.md)) and find a collegue, who approves your pull request. Ask your teammates if your are stucked or if you need help with Git or GitHub.

## Instructions Task 2: changing the format

After updating the version of the content management tool our calender is not displayed correctly anymore. The tool can only process files with a specifiy YAML structure. There are new tickets available for you and your teams ([new tasks to fix format issue](tasks2.md)).


**Follow the instructions of your trainer and have some fun.**
