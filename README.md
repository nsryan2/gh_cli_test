# Gh Demo

This repo is intended as a demonstration for common Github Command Line 
Interface (CLI) uses, and covers how to install the CLI, checking out 
someone else's PR, creating issues and PRs, making a new repo, and 
cloneing an existing repo. This demo assumes some familiarity with git 
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

## Checkout Greg’s PR
`gh pr checkout 1`

## Create an issue 
`gh issue create -a"@me" --title "Bug 4” --body "Nothing works"`

## Creating an issue on the web
`gh issue create --web`

*This is a shortcut that will open your default web browser to a new issue*

## Create a new PR
`gh pr create --assignee “npanczyk” --title "The new new new bug is fixed" --body "Everything works again"`

## Create a new repo
**Never make a new git repo inside of an existing git repo!!**

`cd ..` 

`gh repo create final_demogit`
