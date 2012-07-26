On Git Commits

This repository accompanies a presentation given at 
[Tokyu Ruby Kaigi 05][tokyu05].

## The standard format for git commit messages

By convention, a commit message in git is divided into two parts: a subject and
an optional body. Although git itself doesn't place any restrictions on how you
write commits, many git tools rely on this convention. 

`git format-patch` is one such tool. It allows you to generate a patch email
like the one below.

    From 607164edbae4fe3d9a6068d6f87c72e66d2a140c Mon Sep 17 00:00:00 2001
    From: Paul McMahon <paul@mobalean.com>
    Date: Thu, 26 Jul 2012 17:47:17 +0900
    Subject: [PATCH] Add example about git format-patch

    git-format patch is a tool that lets you generate a patch email from a
    commit.
    ---
     README.md | 3 +++
     1 file changed, 3 insertions(+)

    diff --git a/README.md b/README.md
    index 0051a10..e2f1441 100644
    --- a/README.md
    +++ b/README.md
    @@ -9,5 +9,8 @@ By convention, a commit message in git is divided into two parts: a subject and
     an optional body. Although git itself doesn't place any restrictions on how you
     write commits, many git tools rely on this convention. 
     
    +`git format-patch` is one such tool. It allows you to generate a patch email
    +like the one below.
    +
     [tokyu05]: http://regional.rubykaigi.org/tokyu05
     
    -- 
    1.7.11.3

The first line of our commit becomes the subject of the email, everything blank
line (the third line on down) becomes the body.

[tokyu05]: http://regional.rubykaigi.org/tokyu05

