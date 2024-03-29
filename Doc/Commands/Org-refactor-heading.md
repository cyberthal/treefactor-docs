% org-refactor-heading

treefactor-org-refactor-heading is a minor Org convenience function. It helps you refactor a heading.

Imagine you have a complex heading that covers multiple topics in a disorganized way.

You want to archive a copy of this heading to preserve its original form, then analyze its contents into neatly categorized subheadings.

A classic example would be a chronological record of a sprint. You want to preserve the chronological order for future reference, but you also want to break it down into tasks and categorized reference matter.

treefactor-org-refactor-heading creates a copy of the original heading and appends " | REFACTORED" to the title. It's an historical record now. You don't need to refactor it again.

Then treefactor-org-refactor-heading opens a new window with an indirect buffer showing an "INBOX" heading. This is where you will put the new subheadings.

Now you can grab chunks of the original heading in the first window, and move them to the second window. The goal is to improve the organization; it doesn't have to be perfect. You can always do another refactoring round after this.

To keep track of your progress, delete irrelevant text. No need to worry about losing data, since everything's preserved in the " | REFACTORED" archive copy.

Here's a gif demo:

![](Org-refactor-heading-Zinaries/trs-org-refactor-heading--jabberwocky--output-2019-09-07-02.gif "treefactor-org-refactor-heading Jabberwocky demo")

The gif example heading was very simple. Anybody can break a poem into stanzas without the help of a special function. But we all have complex textwalls in our lives that beg for analysis. This function reduces the friction of doing so, encouraging the user to regularly analyze his complex headings into manageable form.

Org provides a org-archive-subtree command, but it doesn't work well with the Treefactor workflow. Org moves archived subtrees to a different file. Org assumes that the heading's original path will be relevant in the future; Treefactor does not. Org assumes you don't want to move archived headings around the directory tree. Org doesn't make it easy to distinguish folded archive headings from normal headings. So your choices are to refile the entire foo.org_archive file as an indivisible unit, or else mix archived and unarchived headings.

With Treefactor, you don't need to know where you want to refile the heading before you refactor it. You can refile REFACTORED headings the same as any other heading, without needing to open a separate file to find them. You'll never confuse them with current headings.

It is convenient to have REFACTORED headings filed together with the current headings on a given topic. This makes it easy to look up historical references, and easy to decide when a REFACTORED heading can be safely deleted.

If all your archived headings are stored with each other, then you have no idea whether your current information obsoletes them or not. The relevant context is missing. So the Org way is suboptimal.
