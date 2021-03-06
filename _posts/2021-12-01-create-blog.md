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

### Setting up your blog

The first step here is to create the blog structure with Jekyll. Navigate to the directory where you cloned your GitHub repository and enter 
`jekyll new .`

Once this is complete, you can enter `jekyll serve` to start a local web server. You'll be provided with an address that you can view the site at in a browser. 

You should also be able to view the blog via github pages. If you enter the repository name as a URL it should get you there, so in my case it would be https://DrewHalverson.github.io

It can take a minute or two for GitHub to catch up so if you don't see your site wait a bit and check back by refreshing your browser window. 

### Initial Configuration

In your blog directory, there is a file called _config.yml. You'll need to edit it to start customizing content for your blog. Go ahead and open it in your favorite text editor. 

You'll want to change the title to what you want your blog to be called, then update your contact info and the blog description. If you don't want to include social media contact info, you can 
comment those lines out by entering a # at the start of the line. 

You can also update the file titled about.markdown with your own info. 

Go ahead and save your changes and then push them to GitHub in order to update your site. 

### Making your first post

post files live in the _posts directory. The format used for naming them is specific and your post will not update it the name does not match. 

All post files should be names with this format: YYYY-MM-DD-title.md

Go ahead and delete the default post ( or you can remame it so that it still available for reference within the directory but won't show up on the site)

Create a new file with the format discussed previously and open it in your preferred text editor. 

Front Matter in Jekyll refers to information about the post where you can set things like the post title, format, date, and category information. 

The front matter for this post looks like this: 
```
---
layout: post
title:  "Creating a blog with Jekyll and GitHub Pages"
date:   2021-12-01 09:54:54 -0600
categories: howto, blog, ruby, git, jekyll, github
---

```

You can use that as a template to set the information for you own post. 

Jekyll uses [Markdown](https://www.markdownguide.org/) to format posts. 

Go ahead and enter some post content and push it to your repository to deploy it to your blog. 

### Follow up information

This post just touches the surface of a lot of different technologies. Here are some links for further reference if you are interested:

[Jekyll](https://jekyllrb.com/)

[Ruby](https://www.ruby-lang.org/en/)

[WSL](https://docs.microsoft.com/en-us/windows/wsl/about)

[Markdown](https://www.markdownguide.org/)

[GitHub Pages](https://pages.github.com/)




