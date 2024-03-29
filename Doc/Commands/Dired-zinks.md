% org-dired-zinks

treefactor-org-dired-zinks is a minor Org convenience command.

When using treefactor-throw heavily, directory paths can change daily. This breaks path-based links. The solution is to use Org UID links.

Let's say you want to link to a directory, even if its name or contents change. One way is to create a file whose sole purpose is to hold an Org UID link anchor.

treefactor-org-dired-zinks creates this file, and names it Zinks.org. 

The file name was originally Links.org. But when sorting in alphabetical order, that puts the link file in the middle of the content files, which is bad practice. So the filename now starts with Z, to put it at the end of the list.

Here's a gif demo:

![](Org-dired-zinks-Zinaries/dired-zinks--output-2019-09-07-00.gif "dired-zinks demo")

If the directory needs to link to related directories in other parts of the tree, Zinks.org is a good place to store those links.
