% throw

treefactor-throw refiles something to a destination in the next window.

Imagine that the next window holds a row of boxes. You pick up the object at point and throw it into one of the boxes.

In this gif demo, I throw Org headings to different directories in a Dired buffer.

![](Throw-Zinaries/heading-refiling--random-nouns--output-2019-09-06-01.gif "Throw-Zinaries/heading-refiling--random-nouns")

treefactor-throw refiles headings into an Inbox.org file in the chosen directory. If the directory doesn't already have an Inbox.org file, one is created.

treefactor-throw tries to place headings intelligently in files. Normally it appends the heading to the bottom of the file. However, if the file contains a level-one heading, then treefactor-throw assumes that the file is a polished document, not an inbox-style list of headings. It will place the heading immediately before the level-one heading, where it is hard for the user to miss.

treefactor-throw also works on outline headings in other text modes. If the text is not inside an outline heading, then it throws the line at point.

treefactor-throw handles files the same way as text. Here's a demo gif:

![](Throw-Zinaries/file-refiling--random-nouns--output-2019-09-06-15.gif "file refiling--random nouns")

treefactor-throw puts files in a /0-Inbox directory under the chosen directory, so that new files aren't mixed up with pre-existing files.

Lastly, treefactor-throw can throw text to outline headings. Here's a demo gif. This time I'm throwing lines of text instead of outline headings, just for variety:

![](Throw-Zinaries/refiling-to-outline--random-nouns--output-2019-09-06-20.gif "refiling to outline--random nouns demo")

The lines are double-spaced and placed under the selected outline heading:

![](Throw-Zinaries/refiling-to-outline--random-nouns--results--output-2019-09-06-20.gif "refiling to outline--random nouns--results demo")

Double-spacing prevents the user from accidentally appending a line to an existing unrelated paragraph of text.

I've used capitalized search terms to minimize typing in these demos so far. But what if the destination list is difficult to navigate with isearch?

When throwing to an outline, if isearch returns multiple matches, treefactor-throw uses [Avy](https://github.com/abo-abo/avy) for the final selection. 

gif-screencast couldn't capture the Avy overlay, but you can watch how Avy works at the above link. To summarize: Just type the red letter at the line you want.
