% Customizing Treefactor

Inbox.org template - keep transit heading level consistent!
====

tro-refile(-up) creates a file Inbox.org when refiling a heading to a directory that doesn't already have one. It inserts a template into the new Inbox.org file. You can modify this template via the Customization option "Tro Inbox File Header".

The default value assumes that you will always use level-four headings for blind inter-file refiling. It creates a level-three heading to act as a parent for these level-four headings.

You should pick one heading level for blind inter-file heading refiling, and stick to it. Otherwise you may cause unintended parent-child relationships. Child-heading folding may cause you to overlook such mistakes, resulting in further disorganization.

Unintended folding is a general problem for Emacs outline-manipulation commands. If anticipated, it is easily avoided. Otherwise, one can wind up mistakenly deleting important information because it was a folded descendant of an unwanted heading. Like any power tool, an outline permits more powerful mistakes. Always use a git repo to ensure that mistakes are recoverable. 

Aliasing the "tro" prefix
===

Treefactor commands are prefixed with "tro". You can change this prefix to something more convenient. Customize "Tro use alias prefixes" to t. Change "Tro alias prefix" from the default value, "leo", to your preference. Do not set it to "tro", as that will cause a loop when the package is loaded.

Recommended keybindings for speed
====

By putting the following commands on convenient keys, you can refile without thinking about it.

~~~
(global-set-key (kbd "H-f") 'tro-refile)
(global-set-key (kbd "H-g") 'tro-refile-up)
(global-set-key (kbd "C-c k") 'tro-delete-this-buffer-and-file)
(global-set-key (kbd "C-c l") 'tro-org-store-link-fold-drawer)
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
