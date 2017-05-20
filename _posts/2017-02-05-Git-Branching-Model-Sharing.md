---
layout: post
title: "A Good Git Branching Model #CodeSharing"
description: "Sharing session in UNIKOM CodeLabs Division about how to make a good git branching model"
tags: [CodeSharing, Git, Tools]
comments: true
---

### Background Problem
For sharing session in UNIKOM CodeLabs division, I will share my story about how to make a good git branching model. I've been using Git since 3 years ago. I usually just create one branch called `master` (You must be familiar with it). Everything is fine when I work alone. There is different story when I work with the team. Too much code conflict, uncounted pull, integration error are some problems with just one branch exist. <!-- more --> When I was suffering and trying to looking for solution, I found a good reference. Thanks to <a href="http://nvie.com/posts/a-successful-git-branching-model/">`nvie.com`</a> that give me inspiration how to make a good branching model.

<br/>

### Based on My Experience
I've tried some git branching model. Check the list below.

* Push everything to master

    This model has many problems in its implementation. As I mentioned first, the problems are too much code conflict, uncounted pull, integration error.

* Create a branch based on name of team member (Firman branch, Bayu branch, Rizal branch, etc).

    This model has weakness that is the part of job/feature for everyone must be clear in the first of development cycle. 

<br/>

### A Good Git Branching Model
There are two type of branch, main branch and supporting branch.

* Main Branch

    Main branch consist of `master` and `development` branch. `master` is branch for production state and `development' is branch for development state.

* Supporting Branch

    I've decided to make some supporting branch that will help optimizing main branch. Supporting branch consist of `feature` and `hotfix` branch. `feature` branch is a per-feature branch (ex: feature/home_timeline branch) that copied from `development` branch and will merge back to `development` branch after the feature have finished. `hotfix` branch is a branch that will be created if bug encountered in production state and must be resolved as soon as possible. `hotfix` branch is copied from `master` branch, after the bug is resolved `hotfix` branch will merge back to `master` and merge to `development` branch too.

<br/>

### Presentation File
I've created a powerpoint for this. here it is, hope you enjoy.
<center>
    <iframe src="https://onedrive.live.com/embed?cid=D6B4E1978EE2DE1B&resid=D6B4E1978EE2DE1B%213436&authkey=AMgMIIXKuGDsyNs&em=2" width="402" height="327" frameborder="0" scrolling="no"></iframe>
</center>

<br/>

### References

* <a href="http://nvie.com/posts/a-successful-git-branching-model/">http://nvie.com/posts/a-successful-git-branching-model/</a>
* <a href="https://medium.com/hard-work/gitflow-release-hotfix-bddee96fc5c3#.55tx0bgkn">https://medium.com/hard-work/gitflow-release-hotfix-bddee96fc5c3#.55tx0bgkn</a>