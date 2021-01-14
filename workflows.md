## Git bash commands for default workflow

```
git checkout releases/2020

git pull

git checkout –b features/[TICKET ID]

git add [list of changed or created files]

git commit –m „[Ticket ID]-[your description]“

git push –u origin features/[TICKET ID]

git checkout releases/2020
```

## Git Eclipse steps for default workflow

* Select on the project the pop menue: "Team > Switch To > releases/2020"
* Select on the project the pop menue: "Team > Pull"
* Select on the project the pop menue: "Team > Switch To > New Branch ..." and enter the branch name `features/[TICKET ID]`
* Open the "Git Staging" view
* Add the files from the "Unstaged Changes" to the "Staged Changes" (= index)
* Enter your commit message in the format `[Ticket ID]-[your description]` and select the "Commit and Push" button
* Confirm the buttons in the dialog
* Select on the project the pop menue: "Team > Switch To > releases/2020"

| Heading 1 | Heading 2 | Rules |
|-----------|-----------|-----------|
| Noise     | Layouting | * Use Braces <\br> * Group with newline |
| POLS      | Layout    | bla bla |

