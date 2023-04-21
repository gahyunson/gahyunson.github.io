---
layout: post
title:  "github-pages can't satisfy your Gemfile's dependencies"
date:   2023-04-20 15:27:20 +0530
categories: GitHub
---

Here was a problem for build git blog.
The Error message was :
`github-pages can't satisfy your Gemfile's dependencies.`

It was so hard what was the problem. Here is How do I solve.

You have to check gitblog's repository.
1. can see the menu 'Actions', click then there will be workflow runs.
2. Click the pages_build-deployment with error.
3. Click the red X-box.
4. Now, you can see the error message.

My Error message was "Error:  The plainwhite theme could not be found."

My problem : doesn't work on gitpages. But It worked at Local.
Solution : The 'theme' code line change to comment in _configure.yml. 

```
# theme : plainwhite
remote_theme: wrote/plainwhite
```
You can't run both(theme, remote_theme). Have to choose one.

If, you want to run on Local. have to choose 'theme'. 'remote_theme' must be comment.
elif, you want to run on gitpages. have to choose 'remote_theme'. 'theme' must be comment.

If you solve it and git push, 
that need some time for deployment. you just wait unitl deploy.
