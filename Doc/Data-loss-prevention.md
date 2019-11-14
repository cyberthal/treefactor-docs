% Data-loss prevention

Misfiling risk
===

The main risk of using Treefactor is that the user misfiles something - a file under the wrong directory, a heading under the wrong parent, a line under the wrong heading. Further actions taken on the parent object may worsen the situation. For example, one might decide that the parent object is obsolete, and delete it without inspecting its contents.

Treefactor is not terribly complicated, but one should be familiar with Dired and especially outline manipulation before using it in production. It is meant for users who want to go fast and skip manual steps. These are arguably things beginners shouldn't do.

Files are easier than outlines
===

Using Treefactor for outline manipulation currently has somewhat more potential for novice user error than existing Org commands. However, one of the reasons I developed Treefactor was because even as an experienced user I easily become confused when manipulating deep complex outlines, and made misfiling mistakes that resulted in frustration and data loss.

When refiling files and directories in Dired, Treefactor has somewhat less potential for user error than Dired's native commands. Dired is powerful and complex, and it's possible to make mistakes while trying to issue repetitive commands quickly. Treefactor automates and simplifies the most common refile operation, reducing the potential for human error. Because Treefactor logs file destinations and puts them in a separate 0-Inbox directory, refile mistakes are easily recoverable. The same isn't always true in native Dired.

I recommend that beginners learn Treefactor by refiling files and directories in Dired first. When comfortable with the basic concepts, then move on to outline manipulation.

When manipulating outlines, always use a Git repo, and regularly save your work. Magit makes this easy.

Autosave is a less reliable solution when filenames, paths and content are in flux.

**Important**: Read the "Inbox.org template - keep transit heading level consistent!" section on the [Customization](Customization.html) page. It explains how to avoid accidentally misfiling headings under unrelated parents.

Data recovery
===

Wondering where something you refiled went? A message appears in the minibuffer displaying the destination of text and files moved with tro-refile(-up) commands. A log of such messages is available in the *Messages* buffer.

Treefactor automatically saves changes to the user's text data. Give Emacs' undo history generous settings if moving lots of text.

The last block of text that was refiled is saved in the variable tro-object-text until the Emacs session ends. Refiled text is not saved to the kill ring, as this interferes with user yank commands and overcrowds the kill ring.
