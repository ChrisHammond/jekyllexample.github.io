---
layout: post
title: Installing Jekyll locally on Ubuntu and getting it running using Windows Hyper-V
date: '2024-04-18T10:00:15+00:00'
permalink: jekyll-on-ubuntu
description: A blog post that provides easy instructions for installing Jekyll locally on Ubuntu running in a Windows Hyper-V Virtual Machine.
image: BlogPost-4.jpg
categories: [ Jekyll, Tutorial ]
featured: true
comments: false 
---
# *This post is still a work in progress as of 04/18/2024*

1. Create a new Hyper-V VM installing Ubuntu 22.04
2. Run updates for Ubuntu (reboot if necessary)
3. Install GIT
> sudo apt install git
4. Install Bundler
> sudo apt install bundler
5. [Install RBEnv to allow for multiple versions of Ruby](https://www.chrishammond.com/blog/itemid/3178/how-to-upgrade-ruby-on-ubuntu-2204-using-rbenv)
6. Install Jekyll GEM
7. Install other required libraries
> sudo apt install libvips-tools
8. Run Jekyll
> bundle exec jekyll serve
9. Browse to http://127.0.0.1:4000


## Next steps:
1. If you have a large repository, or a large number of repositories, you might run out of disk space on your Hyper-V VM, if that's the case [check out this tutorial for how to expand your Ubuntu disk](https://www.chrishammond.com/blog/itemid/3179/expanding-your-ubuntu-disk-running-in-a-virtual-ma).
