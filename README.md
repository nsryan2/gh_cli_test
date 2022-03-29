# Gh Demo

This repo is intended as a demonstration for common Github Command Line 
Interface (CLI) uses, and covers how to install the CLI, checking out 
someone else's PR, creating issues and PRs, making a new repo, and 
cloning an existing repo. This demo assumes some familiarity with git 
and github; If you are unfamiliar with these tools, we suggest following 
the [git novice](https://swcarpentry.github.io/git-novice/) lesson from 
Software Carpentry. **Do not fork or clone this repo before starting 
(that will be covered in the demonstration).**

## Installing 
Follow the existing guide to 
[install the CLI](https://cli.github.com/manual/installation). 
You may also have to setup 
[SSH keys](https://docs.github.com/en/enterprise-server@3.0/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) 
or some other form of 
[authentication](https://docs.github.com/en/enterprise-server@3.0/authentication) 
before this process works, but it's likely that if you already use git and github 
on your machine you'll be good to go. 

## Clone this repo
`gh repo clone gh_cli_test`

## Enter the repo
`cd gh_cli_test`

## Find out what PRs and Issues there are
`gh pr list`

or 

`gh issue list`

These commands generate a list of the issues or PRs that are active in the repo, and gives you their name, number, who made them, and what branch they are coming from in that person's fork.

## Checkout Greg’s PR
`gh pr checkout 1`

This command will make a branch with the contents of the PR on your machine so that you can play around with it.

## Create an issue 
`gh issue create -a"@me" --title "Bug 4” --body "Nothing works"`

This command will make an issue on the github repository.

## Creating an issue on the web
`gh issue create --web`

*This is a shortcut that will open your default web browser to a new issue*

## Create a new PR
To make a new PR, you need to be on a branch other than main, so first make a branch

`git checkout -b bug-fix`

`gh pr create --assignee “nsryan2” --title "The new new new bug is fixed" --body "Everything works again"`

This command will make a PR on the github repository.

## Create a new repo
**Never make a new git repo inside of an existing git repo!!**

`cd ..` 

`gh repo create final_demogit`

## Other Commands
This is by no means an exhaustive list of the commands you can do with the cli, you can find more in the [gh manual](https://cli.github.com/manual/gh)!
