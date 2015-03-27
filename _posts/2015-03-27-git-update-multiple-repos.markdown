---
layout: post
title:  "Git: Update Multiple Repos"
date:   2015-03-27 00:00:00
permalink: posts/git-update-multiple-repos
---

![Macroons Coffee][1]

Recently, I've been working with a lot of git repos at a time.  I mean a lot. Like more than twenty. . . That's the bad news.

The code news is the code is all passionately crafted and a joy to work with. Which is one of the reasons I try to make sure I'm always working with the latest-and-greatest before diving in.

But, I couldn't see myself running git pull for every single respository. Believe me, I tried. . .

[Git pull][2] itself has it's issues, so I wanted to be mindful of commit merges. In addition, I'm often helping teammates validate new features or bugfixes in bleeding edge branches, so I wanted to make sure I'm always getting the latest-and-greatest remote branches as well. 

By default, git pull helps you do neither particualary well. That's when I ran into the concept of git up.


###Git  Up

With all versions of Git, you can configure a git alias. So I configured an alias called git up:

{% highlight bash %}
git config --global alias.up '!git remote update -p; git merge --ff-only @{u}'
{% endhighlight %}

This alias downloads all of the latest commits from all upstream branches and tries to fast-forward the local branch to the latest commit on the upstream branch. 

Using this technique, I'm able to get all remote branches while keeping the repository's commit history clean. 

But the challenge still remained of how to deal with running git up for multiple git repos.


###Going Full Shell

I use a [shell script][3] to get the job done of updating multiple git repos:

{% highlight bash %}
for repo in repo1 repo2 repo3; do
    (cd "${repo}" && git checkout master && git up)
done
{% endhighlight %}

It's not perfect by any means, but it gets the job done. Some things to look out for. . .

First, you have to add a new repo to your for loop for each new repo you work with. In addition, you need to have previously git cloned the listed repo. Which makes sense because you can't checkout a branch for a nonexistent repo.

Finally, notice the use of the git up alias we created earlier. Combining both technqiues, you're able to reliably update multiple git repos at a time.

If you find yourself needing to update multiple git repos at a time, give this technique a try.



[1]: /images/macroons-coffee.png  "Macroons Coffee"
[2]: http://stackoverflow.com/questions/15316601/in-what-cases-could-git-pull-be-harmful
[3]: http://stackoverflow.com/questions/17099564/make-a-shell-script-to-update-3-git-repos
[4]: https://twitter.com/dhh/statuses/45923430608023552
[6]: http://techoctave.com/c7/posts/90-designer-languages

