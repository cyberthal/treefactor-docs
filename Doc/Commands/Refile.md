% refile

tro-refile refiles something to a destination in the next window.

In this gif demo, I refile Org headings to different directories in a Dired buffer.

![](Refile-Zinaries/heading-refiling--random-nouns--output-2019-09-06-01.gif "Refile-Zinaries/heading-refiling--random-nouns")

tro-refile puts the headings into an Inbox.org file in the chosen directory. If the directory doesn't already have an Inbox.org file, one is created.

tro-refile tries to place headings intelligently in files. Normally it appends the heading to the bottom of the file. However, if the file contains a level-one heading, then tro-refile assumes that the file is a polished document, not an inbox-style list of headings. It will place the heading immediately before the level-one heading, where it is hard for the user to miss.

tro-refile also refiles outline headings in other text modes. It can refile single lines of text, if they are not inside an outline heading.

tro-refile refiles files the same as outline headings. Here's a demo gif:

![](Refile-Zinaries/file-refiling--random-nouns--output-2019-09-06-15.gif "file refiling--random nouns")

tro-refile puts files in a /0-Inbox directory under the chosen directory, so that new files aren't mixed up with pre-existing files.

Lastly, tro-refile refiles text to an outline heading. Here's a demo gif. In this case I am refiling lines instead of outline headings:

![](Refile-Zinaries/refiling-to-outline--random-nouns--output-2019-09-06-20.gif "refiling to outline--random nouns demo")

The lines are double-spaced and placed under the selected outline heading:

![](Refile-Zinaries/refiling-to-outline--random-nouns--results--output-2019-09-06-20.gif "refiling to outline--random nouns--results demo")

Double-spacing prevents the user from accidentally appending a line to an existing unrelated paragraph of text.

I've used capitalized search terms to minimize typing in these demos so far. But what if the destination list is difficult to navigate with isearch?

When refiling to an outline, if isearch returns multiple matches, tro-refile uses [Avy](https://github.com/abo-abo/avy) for the final selection. I couldn't capture the Avy overlay in gif-screencast, but you can see how it works at the preceding link. To summarize: Just type the red letter at the line you want.
