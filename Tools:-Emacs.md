By default, `emacs` will use spaces to indent your C code.

Of course, you don't want that.

To tell emacs to use `tabs` instead, you just need to put the following lines in the file `~/.emacs` (If it doesn't exist, just create it):

```Emacs
(setq c-default-style "k&r"
      c-basic-offset 8
      tab-width 8
      indent-tabs-mode t)
```

___

If you want to highlight lines exceeding 80 characters and trailing whitespace, you can add this to your `~/.emacs`:

```Emacs
(require 'whitespace)
(setq whitespace-style '(face empty lines-tail trailing))
(global-whitespace-mode t)
```