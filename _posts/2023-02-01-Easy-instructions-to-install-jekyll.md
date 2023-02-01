---
layout: post
title: Easy instructions for installing Jekyll 
date: '2023-02-04T10:00:15+00:00'
permalink: easy-installation-instructions-for-jekyll
image: BlogPost-4.jpg
categories: [ Jekyll ]
featured: true
---
The goal for this blog post is to provide easy instructions for installing Jekyll. Th

If you follow these steps, you should be able to create a new Jekyll web site utilizing GitHub and GitHub Pages to host your repository and web site.

We will walk you through the process of cloning the repository, making some changes to the site to configure it to be your own, and then ultimately getting your website published using your own custom domain name. 

A couple of assumptions to start:
1. [You have a GitHub account created](https://github.com/signup).
2. You have already purchased a custom domain name to use (you can bypass this and create a site using SITENAME.github.io)
3. You have Git tools installed (if you're using Windows, use Git For Windows)
4. You have [Visual Studio Code](https://code.visualstudio.com/) installed, or some other text editor that you're comfortable with.


## Precursor


## Instructions

1. Create a new Organization on GitHub 
    A free organization account will be sufficient. For our example organization, we will used JekyllExampleWeb (JekyllExample was already taken). 
    This previously was something I believe was necessary to use GitHub pages, but based on my experience I am not convinced it is required anymore, meaning you can also create repos for GitHub pages under your personal account (ex:ChrisHammond/jekyllexample.github.io)
2. [Create a Fork of the JekyllExample repository](https://github.com/ChrisHammond/jekyllexample.github.io/fork)
    Create the fork within your new organization that you created in step 1.
3. Rename the repository to match the domain name that you want to use for GitHub Pages
    As soon as you fork the repository, you can rename it. You will want to rename it to match the domain name that you want to use for GitHub Pages, for example we use jekyllexample.com, so the repository is jekyllexample.github.io. 
4. Clone the repository to your local machine for editing
    You can clone the repository to your local machine using the following command, (assuming you have Git installed, start up Git Bash and then navigate to the folder where you want to clone the repository to)
    ```bash
    git clone https://github.com/ORGANIZATION/SITENAME.github.io.git
    ```
    Where SITENAME is the name of your repository that you modified in Step 3.
5. Open the repository in Visual Studio Code
    You can open the repository in Visual Studio Code using the following command:
    ```bash
    code SITENAME.github.io
    ```
    Where SITENAME is the name of your repository that you modified in Step 3. 
5. Change the _config.yml file
    This file has a number of variables for options for your site, such as Title, Description, Author, etc. You will want to customize these to start to brand and name your site.
    If you're using Google Analytics you can configure the MEASUREMENT ID here as well.
6. Edit the CNAME file in the root of the repository to match your custom domain name
    If you're not using a custom domain name, you can delete this file.
7. Commit your changes to the GitHub repository and push them.
    ```bash
    git add .
    git commit -m "Some updated comment about the commit here"
    git push
    ```
    You may be prompted to configure your GitHub credentials at this point, [here's an approach on how to do that](https://stackoverflow.com/questions/46878457/adding-git-credentials-on-windows).
8. Configure the repository settings for GitHub Pages and Workflow to allow for deployment
    In the GitHub Repository Settings, you will want to configure the following:
    - Under the GitHub Settings find the GitHub Pages section
    - Under Source choose "Deploy from a branch"
    - Under Branch choose "main" and "/(root)"
9. Configure your DNS for your domain to point to GitHub pages
    You will need to do this before step 10 so that GitHub can verify and find your custom domain name configured properly. 
    I use CloudFlare for my domains, so the DNS entries are configured as follows:
    {% picture "images/cloudflaredns.JPG" class="img-fluid lazyimg" --alt "DNS Settings for CloudFlare"  %}
10. Configure your custom Domain Name
    - Under the GitHub Settings find the GitHub Pages section
    - Under Custom Domain, enter your custom domain name (ex: jekyllexample.com)