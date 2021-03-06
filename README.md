# Finnish keyboard relief for OSX Emacs #

If you want to use alt (option) key as meta and also use Finnish keyboard layout, it can get quite frustrating. Same problem exists in many other european keyboard layouts as well.

You can get a bigger picture of the issue by reading this StackOverflow question and answers:

http://stackoverflow.com/questions/500602/os-x-terminal-meta-key-alt-functionality-at-t
he-same-time

The solution which I find bearable is borrowing few files from Aquamacs and making a few tweaks in your emacs init file. 

Here's what I've done:

    (defun aq-binding (any) nil)
    (load  "~/.emacs.d/aquamacs-tools.el")    
    (load  "~/.emacs.d/emulate-mac-keyboard-mode.el")
    (setq emulate-mac-finnish-keyboard-mode t)
    (setq mac-right-option-modifier nil)

Not sure what the first line is doing, second and third are self-explanatory and the last line makes your right alt to behave as a normal alt in case your fancy new meta/alt key fails to produce characters in some corner cases.

The files emulate-mac-keyboard-mode.el and aquamacs-tools.el are borrowed into this repository from the Aquamacs repository (https://github.com/davidswelt/aquamacs-emacs).

