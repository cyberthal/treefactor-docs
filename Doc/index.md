% Treefactor - refactor prose and incrementally refile

Treefactor is an Emacs package that restructures the directory tree and refactors outlines.

> There are only two hard things in Computer Science: cache invalidation and naming things.
> 
> -- Phil Karlton

Treefactor makes naming things easy, by breaking the process down into many small quick steps.

It conceptualizes the directory tree and outlines within files as one unified meta-outline.

Treefactor assumes that the user knows the current information context very well, but that his knowledge of the rest of the meta-outline degrades as distance from the current location increases.

Therefore, Treefactor provides the user with refiling commands that cover the smallest possible distance. The shorter a refile, the more likely it is to be an improvement rather than a mistake.

Treefactor's other commands are mostly tweaks to org-mode to support this workflow, which differs from Org's philosophy.

Treefactor's goal is inductive meta-outline evolution. I use Treefactor to manage my Textmind, a 1/3 gigabyte text exobrain Git repo that can comfortably process 10k words per day. Daily intake varies between 1-20k words, usually. I read a lot, and Treefactor has no trouble keeping up. Other personal information managers always choked on the volume.

If you are learning about Treefactor for the first time, please read this site in the order listed on the Table of Contents sidebar. Each command has at least one gif demo that will help you understand what it does.

This is a power tool that quickly moves text and files around the directory tree. Please learn how it works before using it in production, or you may misfile important text and files. I recommend using it with version control so that you can revert undesired changes. I use Git for text and git-annex for files.

This site is up-to-date for Treefactor version 2.0.0

The code for this site is hosted at [Github](https://github.com/cyberthal/treefactor-docs).

This package would not have been possible without the inspiration of [BrainStorm](http://brainstormsw.com).
