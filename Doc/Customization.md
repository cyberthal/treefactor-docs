% Customizing Treefactor

Inbox.org template - keep transit heading level consistent!
====

treefactor-throw and treefactor-up create a file Inbox.org when refiling a heading to a directory that doesn't already have one. They insert a template into the new Inbox.org file. You can modify this template via the Customization option "Treefactor Inbox File Header".

The default value assumes that you will always use level-four headings for blind inter-file refiling. It creates a level-three heading to act as a parent for these level-four headings.

You should pick one heading level for blind inter-file heading refiling, and stick to it. Otherwise you may cause unintended parent-child relationships. Child-heading folding may cause you to overlook such mistakes, resulting in further disorganization.

Unintended folding is a general problem for Emacs outline-manipulation commands. If anticipated, it is easily avoided. Otherwise, one can wind up mistakenly deleting important information because it was a folded descendant of an unwanted heading. Like any power tool, an outline permits more powerful mistakes. Always use a git repo to ensure that mistakes are recoverable. 

Aliasing the "treefactor" prefix
===

An alias creates an additional name for a command. Treefactor commands are prefixed with "treefactor". This prefix is 10 characters long, which can be inconvenient to type repeatedly.

Treefactor lets you easily alias a shorter prefix. Customize "Treefactor use alias prefixes" to t. The default for the first alias is "tro", which is a phonetic misspelling of "throw".

Do not set an alias to "treefactor", as that will cause a loop when the package is loaded.

Recommended keybindings for speed
====

By binding the following commands to convenient keychords, you can refile without thinking about it:

~~~
(global-set-key (kbd "H-f") 'treefactor-refile)
(global-set-key (kbd "H-g") 'treefactor-refile-up)
(global-set-key (kbd "C-c k") 'treefactor-delete-this-buffer-and-file)
(global-set-key (kbd "C-c l") 'treefactor-org-store-link-fold-drawer)
(global-set-key (kbd "H-a") 'other-window)
(global-set-key (kbd "H-w") 'outline-up-heading)
(global-set-key (kbd "H-e") 'outline-previous-visible-heading)
(global-set-key (kbd "H-r") 'outline-next-visible-heading)
(global-set-key (kbd "H-d") 'org-narrow-to-subtree)
(global-set-key (kbd "H-s") 'widen)
(global-set-key (kbd "H-1") 'spacemacs/toggle-maximize-buffer)
(global-set-key (kbd "H-2") 'delete-window)
(global-set-key (kbd "H-3") 'split-window-right)
(global-set-key (kbd "s-i") 'ido-dired)
~~~

I use a Microsoft Natural Ergonomic Keyboard. I set the Appkey to Hyper and the Winkey to Super.
