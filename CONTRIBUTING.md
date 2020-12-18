# Git Workflow For Outside Contributions

> Thank you for wanting to help, please follow these guidelines. We only accept pull requests for current issues, as you will see in the documentation below you will need the issue# during your pull request.

If you don't have git on your machine, [install it](https://help.github.com/articles/set-up-git/).

## First Steps

Please make note of the current issue# you want to work on, you will need this later.

Leave a comment on that issue with a brief summary of what you plan to do to fix the issue.

## Fork this repository

Fork this repository by clicking on the fork button on the top of this page.
This will create a copy of this repository in your account.

## Clone the repository

Now clone the forked repository to your machine. Go to your GitHub account, open the forked repository, click on the clone button and then click the _copy to clipboard_ icon.

Open a terminal and run the following git command:

```
git clone "url you just copied"
```

where "url you just copied" (without the quotation marks) is the url to this repository (your fork of this project). See the previous steps to obtain the url.

> For example:

```
git clone https://github.com/this-is-you/git-help-me.git
```

Where `this-is-you` is your GitHub username. Here you're copying the contents of the code-experiment-website repository on GitHub to your computer.

## Create a branch

Change to the repository directory on your computer (if you are not already there):

```
cd git-help-me
```

Now create a branch using the `git checkout` command:

> Please make sure the branch-name has the issue#number

```
git checkout -b <add-your-new-branch-name>
```

> For example:

```
git checkout -b issue#10
OR
git checkout -b yourName-issue#10
```

## Make necessary changes and commit those changes

Now open the code into your favorite editor and start making any changes you feel are needed to fix the issue.

Please commit your code frequently and keep within the scope of the issue. For example if your issue was fixing a bug with a form, don't go styling the navbar at the same time.

## Push changes to GitHub

Push your changes using the command `git push`:

```
git push origin <add-your-branch-name>
```

replacing `<add-your-branch-name>` with the name of the branch you created earlier.

## Submit your changes for review

If you go to your repository on GitHub, you'll see a `Compare & pull request` button. Click on that button.

Change the title and description to explain your changes. Please make sure to use one of the keywords in your description in order to link your pull request to the issue.

> Example:

- Title: [issue#112] Refactor variable with null value
- Description: There was an issue with the variable name causing a null value, I refactored the variable name and it fixes #112

Don't forget to use one of the linking keywords. You can learn more about linking pull requests at the [GitHub Docs](https://docs.github.com/en/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword).

- close
- closes
- closed
- fix
- fixes
- fixed
- resolve
- resolves
- resolved

Now submit the pull request.

A team member will review your changes, please keep an eye out for any requested changes during this review. Once all the code is working and they like the changes, they will merge it into the repo. Thank you for the help!


## What To Do After Your Changes Get Approved

> Don't forget to sync your main branch of the fork to the original repository!  For a more detailed instruction about this, read this article.  https://www.freecodecamp.org/news/how-to-sync-your-fork-with-the-original-git-repository/

1. Add a new remote upstream repository
    > You only need to do this for the initial sync.
    ```
    $ git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
    ```
    $git checkout main
2. Sync your fork
    > You need to do this after each successful merge
    ```
     $git checkout main  
    $ git fetch upstream
    $ git checkout master
    $ git merge upstream/master
    $ git push origin
    ```
