% Roadmap

This page describes planned changes to Treefactor.

Meta-outline continuity
===

Right now the Treefactor meta-outline is imperfectly joined. There's a discontinuity when jumping between files and outlines. The below design changes fix this problem.

One level-one heading per file
-----

The goal is to have only one level-one heading per file. This permits quick verification that the file's outline is in a properly formatted state. If there are two or more level-one headings, you know something has gone wrong.

Contrast with a file that has several level-one headings. Now it is difficult to obtain an overview at a glance, if only because the level-one headings are in a face that is too large. Outline navigation of multiple level-one headings is awkward. One cannot use outline-up-heading to jump above them. If there is text before the first heading, then there is no way to jump to the first heading quickly. One must use global outline visibility cycling to affect all the level-one headings, because parent outline visibility cycling is unavailable. 

Level-two headings are also much larger than body text, so potential problems with the outline can be pushed below the fold when you expand a level-one heading with other level-one headings below it. The boldness of level-one headings makes them difficult to read carefully when adjacent. The face isn't designed for that scenario.

Visibility when buffer opens
----

The title of the level-one heading repeats and expands upon the filename. 0-Inbox.org is generated with "[relative path]/0-Inbox.org" as the level-one heading.

Set the level-one heading properties to display level-two folded headings when the file opens. This allows a good amount of information to fit on the screen at a time. If the first level-two heading is 0-Inbox, you know there are potentially new headings to sort.

The 0-Inbox heading
---

If present, 0-Inbox is the first of the child headings of a given parent. Headings newly placed into the file will arrive as level-three children of the level-two 0-Inbox. From there, they can be sorted into the outline in the same way Treefactor does Dired refiling of files.

Promoting a heading out of a file not named 0-Inbox.org moves it into 0-Inbox.org in the same directory.
Promoting out of a file occurs only if the heading is level-two, or a level-three child of the level-two 0-Inbox.

When filing a heading to a file, if no level-one heading exists, one will be created, titled with the file's name. If multiple level-one headings exist, the first one will be used.

Thus the default transport level of headings will become level-three, instead of level-four as currently.

I'll also need an outline command to dump the children of the 0-Inbox heading as appended child headings of the same parent as 0-Inbox, then delete 0-Inbox. Use this command when all the headings in a 0-Inbox heading are at the correct destination.

Inbox.org should become 0-Inbox.org, to enhance its visibility in Dired.

The above changes can be implemented by expanding tro-refile(-up).

Treefactor outline minor mode
---

How the planned Treefactor outline minor mode should work:

Single-keychord Dired-style navigation of an outline should be possible in Treefactor outline-mode. Dired automatically handles outline widening and narrowing as it traverses the directory tree. The mode should not interfere with the normal Org outline manipulation commands, but may prevent text insertion except at heading titles.

These changes will reduce the current incentive towards many small files, as they will offer no ergonomic benefit vs complex single-file outlines. Currently the awkwardness of Emacs in-buffer outline manipulation makes Dired a preferable outliner.

Misc
===

Make tro-object-text a ring

If a heading refile would make a heading the child of the refiled heading, quit with an error.

Future versions may add tro-prefixed functions and customizations from my [Spacemacs personal layer](https://github.com/cyberthal/spacemacs-personal).
