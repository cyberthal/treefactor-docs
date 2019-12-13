% Treefactor - restructure your messy Org documents

Introduction
---

Treefactor is an Emacs package that defines a joint org-mode/Dired workflow for restructuring your messy Org documents.

Treefactor breaks text into logical outline headings, then refiles those headings.

Treefactor conceptualizes the directory tree and outlines within files as one unified meta-outline. It facilitates restructuring that outline.

Rather than trying to refile from the current location to the final destination in one hop, Treefactor uses inductive incremental refiling. This lets you rapidly refile many objects in the right direction, one step at a time.

(If the above introduction was too abstract, and you're experienced with Emacs, then skip ahead to the "Commands" section. Then come back here.)

What it can do, exactly
---

Technically, Treefactor can refactor any text into an outline. In practice, I only refactor Org files, since that's where I keep almost all my prose. Treefactor is focused on Org mode, but many of Org's commands work on outlines in other modes.

In addition to headings, Treefactor can refile files in Dired. I use Treefactor when I need inductive sorting. Typically this means "user" files of the kind stored in ~/Documents, ~/Downloads, etc. These files cover a dynamic range of topics, so I categorize them inductively.

Why inductive?
---

Inductive incremental refiling is useful when user knows the current information context well, but his knowledge degrades as distance from the current location increases.

This is quite common. For example, imagine you're moving to a new house. Right now you're packing up the old house. Do you know exactly where all your stuff should go at the new house? Of course not. You just pack up all the garage stuff into "garage" boxes, and defer finer organization until it's time to unpack them.

Treefactor is like a magic wand you point at the stuff in your garage. You say "garage," and it magically jumps into the garage box. It automates repetitive actions in the workflow.

Treefactor gives the user refiling commands that cover the smallest possible distance. The shorter a refile, the more likely it is to be an improvement rather than a mistake. Simple decisions are exponentially easier to make than complicated ones.

Treefactor's other commands are mostly tweaks to org-mode to support this workflow, which differs from Org's philosophy.

How to read this site
---

If you are learning about Treefactor for the first time, please read this site in the order listed on the Table of Contents sidebar. Each command has at least one gif demo that will help you understand what it does.

Treefactor's goal is inductive meta-outline evolution. I use Treefactor to manage my Textmind, a 1/3 gigabyte text exobrain Git repo that can comfortably process 10k words per day. Daily intake varies between 1-20k words, with 2.5k a typical number. I read a lot, and Treefactor has no trouble keeping up. Other personal information managers always choked on the volume. Here is a [template](https://gitgud.io/Bibliodemos/textmind-template) you can use to start your own Textmind.

Treefactor is a power tool that quickly moves text and files around the directory tree. Please learn how it works before using it in production, or you may misfile important text and files. I recommend using it with version control so that you can revert undesired changes. I use Git for text and git-annex for files.

Links and version
---

This site is up-to-date for Treefactor version 3.0.1

The code for this site is hosted at [Github](https://github.com/cyberthal/treefactor-docs).

This package would not have been possible without the inspiration of [BrainStorm](http://brainstormsw.com).
