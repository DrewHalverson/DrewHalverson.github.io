---
layout: post
title:  "Adding a Custom Domain with SSL to GitHub pages"
date:   2022-04-02 11:15:34 -0600
categories:
---

I've been using GitHub Pages to host this blog for several months and recently
realized that the site was not secured with an SSL certificate. After some trial 
and error, I managed to get it set up. I use Cloudflare for DNS so will be detailing
how to configure DNS records on their site. This assumes that there is a custom domain
name reserved for use in this context.

# Github Settings

Navigate to the repository where your site is hosted. Once there, click on the settings
icon. Scroll down and click on the Pages link on the left. 

Under Custom Domain, enter your domain name and click Save. 

# DNS Configuration

Log in to your Cloudflare account and navigate to the domain you want to configure. 
If you haven't set up the domain previously you will need to add it via the Add a Site button and configure 
the domain to point to Cloudflare. 

Click on DNS in the left column and click the Add record button. 

Configure a record: <br>
+ Type should be A 
+ Name should be your domain name (i.e.- example.com) 
+ IPv4 address should be the first address found [here under "Configuring an apex domain".](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-a-records-with-your-dns-provider) 


Repeat this process for each of the four addresses. 

Configure a CNAME record to resolve www for your domain:  <br>
* Type should be CNAME 
* Name should be www 
* Target should be your_github_username.github.io 

Once the DNS records are configured, click on SSL/TLS in the sidebar and select the Full 
radio button to enable Full encryption mode. 

Select Edge Certificates under SSL/TLS and scroll down. Always use HTTPS should be toggled on
as should Automatic HTTPS Rewrites. 

Once those setting are updated, you should have a secure site. 
