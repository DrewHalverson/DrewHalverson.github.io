---
layout: post
title:  "Archiving Git Repos"
date:   2022-01-14 08:34:54 -0600
categories:
---

In preparation for classes starting in a few days, I wanted to clean up my GitHub repositories and set up some new ones
for the classes I will be taking. 

Git/GitHub doesn't appear to have an intuitive way to do this. 

The first solution I tried was to move all of the folders for the repos I wanted to archive to a new archive repo. I 
cloned the new archive repo, moved the folders on my local machine, and pushed the changes to GitHub. This resulted in 
the directoried appearing in the new repo but the content in the directories being inaccessible. 

When I pushed the changes to the new repo, there was a warning about pushing the old repos to the new one and a suggestion
to use submodules. I probably won't work with the content I am archiving again, but I may want to view it in the future 
for reference. At any rate, I felt submodules was not the best solution for this problem. 

I removed the .git directories from the repos I was trying to move and then tried the push again. This worked, but was
a bit tedious as each .git folder needed to be manually removed. 

I asked a mentor about the problem and she suggested that I could use git merge -allow-unrelated-histories to achieve
the same result without the manual file deletion. (Thanks, Beth!)

I am also going to be more intentional about how I set up repos in the future to try to keep things on GitHub as organized 
as possible. I had multiple repos for different parts of an online program I was working through and I could have just 
created a single repo for the program and organized with subfolders within that repo. 

