---
layout: post
title: Building an academic website
description: "How I built my academic website using Github Pages, Jekyll, Minimal Mistakes, JabRef, and PubListX."
comments: false
---

How did I build this personal website? I found a blog post ([_My experience in building a personal academic website_](https://jponttuset.cat/building-an-academic-website/)) written by Jordi Pont-Tuset, forked Jordi's GitHub [repository](https://github.com/jponttuset/jponttuset.github.io) and made mine. That is it:)

<br />
Basically, the website is built by Jekyll, a static site generator, using the [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) theme. In the following, I will briefly go through the steps (on my RPM-based OS) to build a GitHub page. You may read the Jordi's [blog post](https://jponttuset.cat/building-an-academic-website/) for more details. 


#### 1. Run the website locally

```
# Clone the repository
git clone https://github.com/jponttuset/jponttuset.github.io homepage && cd homepage

# Install Jekll
gem install jekyll

# Run the website
bundle install
bundle exec jekyll serve
```

Now you should see the website at `localhost:4000`. Chances are you encounter some issues. Two basic ones will be fixed using the following commands and the rest with the help of StackOverflow:)

```
# Fix the dependency error
bundle install --path vendor/bundle

# Kill jekyll process
ps aux |grep jekyll |awk '{print $2}' | xargs kill -9
```


#### 2. Customize your website
There is a ton of different things you can do to customize your website. It is a good idea to first get familiar with the [structure](https://mmistakes.github.io/minimal-mistakes/docs/structure/) of the Minimal Mistakes theme in which `_layouts`, `_includes`, and `_config.yml` are the most important folders/files. In addition, you can look into the [GitHub toturial](https://github.com/github/personal-website/blob/master/README.md) on building a personal website. Finally, you can check out [this pull request](https://github.com/hmdfsn/hmdfsn.github.io/pull/1/files) for my initial updates on top of the sample website.


#### 3. Run the GitHub page
Once you are happy with your customized website, create a GitHub repository named `username.github.io` (where `username` is your actual GitHub username), and push the local website to this repository. In just a few seconds, your website is up and running at `username.github.io`. You can learn more about GitHub pages [here](https://guides.github.com/features/pages/).


### Easy-to-mantain publications page
Per Jordi's [suggestion](https://jponttuset.cat/building-an-academic-website/#easy-to-mantain-publications-page), you can easily collect and organize your publications using a free cross-platform tool called [JabRef](http://www.jabref.org/). That helps you to directly export publications from JabRef to your webpage using [PubListX](https://github.com/fitheart/PubListX). A quick setup is as follows:

```
Step1: Install JabRef
$ dnf install jabref

Step2: Download and extract PubListX
$ wget https://github.com/fitheart/PubListX/archive/master.zip && unzip master.zip

Step3: Add PublistX to JabRef
- Open JabRef and select menu Options | Manage custom exports.
- Click Add to create a new export.
- Enter PubListX as the 'Export format name' and .html as the 'File extension'.
- Click Browse and select file publistx.layout in the PubListX directory as the main layout file.
- Click 'Save exporter' then OK. Now if you select menu File | Export, PubListX should be available in the export list.
```
