# Git With Multiple People


## Instructions

In this scenario you will work with your project team to become comfortatble with more advanced git. You will each work off of the same repository and perform a series of operations of Git operations.

There are 3 roles in this scenario.

1. The Pizza Party Lover
2. The French Fry Fanatic
3. The Project Manager

Work with your team to decide who wants to be which. If you're the project manager then continue reading to the other two out loud. If you're one of the other two then wait for close this page and await instructions from your project manager. If only two of your team has showed up then both of you should continue reading this document together. If you are the only one in your group, please try to find another group to join in temporarily for the rest of lab.

## Scenario

### Make a Branch

If you haven't already, clone this repository to your local machine and navigate to that directory with your terminal. Both the Pizza and French-Fry roles should be in this directory before moving forward. The repository should be the **same** url for the 3 of you, i.e. only 1 repo per group.

You will notice there's only two files in the directory README.md and food.md. 

If you are the Pizza Party Lover create the "branch" `pizza` via the following command

`git branch pizza`

If you are the French Fry Fanatic create the "branch" `frenchfry` via the following command

`git branch frenchfry`

A branch is a copy of the entire git repository at a particular commit. In git you can have many branches as you want to split your code into multiple versions. You will see why this is useful soon.


If you are the Pizza Party Lover change to the `pizza` branch via the following command

`git checkout pizza`

If you are the French Fry Fanatic change to the `frenchfry` branch via the following command

`git checkout frenchfry`

(Manager wait for your teammates to complete your instructions and then continue)

### Make a Change


If you're the Pizza Party Lover open up the `food.md` file and change first line of the file to be that of your favorite food (Pizza).

French Fry Fanatic you do the same for your favorite (French Fries).

Both of you save your files and wait for further insturctions.

The Pizza Party Lover should now `add` the files to their git staging area and then save their progress by `commit` their changes with a message (`-m`) of 'Pizza'.

The French Fry Fanatic Should do the same.

(Manager wait for your teammates and then continue)

### Create Commits

The Pizza Party Lover should now `add` the files to their git staging area and then save their progress by `commit` their changes with a message (`-m`) of 'Pizza'.

After doing so, the Pizza Party Lover should return to the `main` branch (via `checkout`) and open up the `food.md` file. What did you observe? All 3 members should look at the Pizza Party Lover's screen.

You will notice that the change they made is gone. This is because the commit to save this change was made on the `pizza` branch and not the `main` branch.

The Pizza Lover should now merge the changes from the `pizza` branch back to main with `git merge pizza` this will pull the changes from the `pizza` branch into the `main` branch. Note this would pull **all** the commits different from `main`, not just the last one.

The French Fry Fanatic should perform the acctions the pizza member did. `add`, `commit`,`checkout`,`merge`

(Manager wait for your teammates and then continue)

### Synchrnoizing everything

**Important ensure the next step is only performed by the pizza member. The French Fry Fanatic should follow along but not take action**

Now the Pizza Party Lover should push their changes on `main` to GitHub with `git push origin main`

After this completes succesfully, the French Fry Fanatic should do the same. What happens? Everyone should now look at french fry's screen. Pizza should continue looking off of French Fry's screen for the rest of the exercise

You will see a message that says the push is denied because the branch is "behind." This is because there are changes on GitHub that do not exist on French Fry's local device. To solve this we need to grab the changes via a `git pull origin main` perform this command and then proceed carefully to the next steps.

French Fry's git branch is now in a crazy intermediate state where there are multiple correct versions of the code that are in contradiction to each other. These contradictions are called "conflicts" and we need to "resolve" them by addressing all of the files and then commiting our resolutions.

Open up the `food.md` file and observe what has happened. There are two Versions of the code separated by `<<<` and `>>>` delinations. 

Now the 3 of you must decide together what should go on line 1 of this file? Is it pizza, french fries, or perhaps something else entirely. Delete all of the lines of code and make it how you want it.

Now `add` and `commit` the change and `push` it to GitHub.

With that you're done. You've all officially resolved your first merge conflict! 🎉

Complete the attendance form: https://forms.gle/Cj53199pW7sPJcZp6 and use the rest of this time to work on Milestone 1.







