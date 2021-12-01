---
layout: post
title:  "Creating a blog with Jekyll and GitHub Pages"
date:   2021-12-01 09:54:54 -0600
categories: howto, blog, ruby, git, jekyll, github
---

### Create a GitHub account and a new repository

Head to [github](github.com) and create a new account or log in to your existing one. 

We'll need to set up a repository for your blog. Click on the repositories tab once you are logged into your account 
and then click the New button. 

In order for this to work with GitHub pages, the naming format for the repository needs to match the following:

username.github.io

So my repository would be named DrewHalverson.github.io

Now you'll want to clone the repository to your local computer. GitHub has documented that process [here](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)

### Install Ruby, Bundler, and Jekyll

You'll need to install Ruby on your local system in order to use Jekyll. If you don't already have it installed, then [follow this tutorial](https://www.ruby-lang.org/en/documentation/installation/)

Windows users will definitely want to consider using WSL for this (and for most dev stuff, arguably). [This is a good guide](https://medium.com/@janelgbrandon/a-guide-for-using-wsl-for-development-d135670313a6) for setting up WSL.

After you get Ruby installed, you'll also need Bundler. If it is not installed yet run `gem install bundler`

Finally, we'll install Jekyll. We'll use a Gem called gitHub-pages that includes Jekyll and all of the tools you will need to set up your blog. 
To install, type `gem install github-pages` in a terminal.

###Setting up your blog

The first step here is to create the blog structure with Jekyll. Navigate to the directory where you cloned your GitHub repository and enter 
`jekyll new .`

Once this is complete, you can enter `jekyll serve` to start a local web server. You'll be provided with an address that you can view the site at in a browser. 

You should also be able to view the blog via github pages. If you enter the repository name as a URL it should get you there, so in my case it would be https://DrewHalverson.github.io