---
title: "Github connect terminal."
date: 2024-06-30T13:29:19+02:00
url: /01-github-connect/
# image: images/2024-thumbs/01-asus-g752vl-dissasembly.jpg
categories: 
  - how to
tags: 
  - how to
  - laptop
  - dissasembly
showtoc: true  # Table of content to hide (false) or show (true).
draft: true  # Show (false) or hide (true) on page.
language: "English"
---

    hugo version

## Get your GitHub personal access token

To create a personal access token in GitHub, follow these steps (`LMB` is `Left Mouse Button`):

1. Log into your GitHub profile (probably in your web browser).
2. Under your GitHub user profile (not the repository profile) LMB click the `Settings`.
3. Scroll down and LMB click the `Developer Settings`.
4. LMB click the `Personal access tokens`.
5. LMB click the `Tokens (classic)` link.
6. If token is not alerady created, LMB click on the `Generate new token` and provide your password again if required.
7. In the `Note` field type a name for the token.
8. Set the access token’s expiration timeout to `No expiration` but if you want to renew token periodically, you will set.
9. LMB click the checkbox for every permission scope to give your GitHub token full repository access.
10. LMB click `Generate token`.
11. Copy the token to use it as the password when you do a Git push to GitHub.

## Basic git prepare

First open Terminal (on Linux) or Git Bash (Windows) or what ever utility you will use, that depends on the Operating System and tool you use.

1. Initialize the project

    To initialize use this command:

        git init
    
    This code creates new subfolder `.git` that generates local git repository on your computer only and not the Github page! It also tracks your project changes, info to put your files on the github site, etc..

    &nbsp;

2. Identify yourself
  
    Add your name and email info. 

        git config --global user.name "YOUR NAME"
        git config --global user.email "YOUR@MAIL.COM"

    *Replace*: 

    - `YOUR NAME` with your name (example: `John Smith`)
    - `YOUR@MAIL.COM` with your email (example: `john.smith@gmail.com`).
    
    &nbsp;

3. Connect to remote github repository

        git remote add origin https://github.com/USERNAME/REPOSITORY-NAME.git
     
    You can find full link inside your GitHub repository settings web-page. 

    If you added the repository corectly, you can check it with: 
   
        git remote -v

    Response should be something like this:

        origin https://github.com/USERNAME/REPOSITORY-NAME.git (fetch)
        origin https://github.com/USERNAME/REPOSITORY-NAME.git (push)

    *Replace*: 

    - `origin` is an alias for your repository and you can use what ever you want. Alias will be used later to send data to GitHub. 
    - `USERNAME` write your username (example: `john`). 
    - `REPOSITORY-NAME` write your repository name (example: `website`) 

4. Log in with a token

    git remote set-url origin https://USERNAME:TOKEN@github.com/USERNAME/REPOSITORY-NAME.git

    *Replace*: 

    - `USERNAME` write your username (example: `john`). 
    - `TOKEN` write your personal token. Check []() 
    - `REPOSITORY-NAME` write your repository name (example: `website`) 

            git status
            
            git add .
            
            git commit -m "COMMIT TITLE"
            
            git push origin

## Resources

https://www.youtube.com/watch?v=qYoc07Da6kg&list=PLbvZxzmdNckwzAHkjkHcIVAEbVh7A8l40&index=3
