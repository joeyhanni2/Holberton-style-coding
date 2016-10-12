By default, `emacs` will use spaces to indent your C code.

Of course, you don't want that.

To tell emacs to use `tabs` instead, you just need to put the following lines in the file `~/.emacs` (If it doesn't exist, just create it):

```Emacs
(setq c-default-style "k&r"
      c-basic-offset 8
      tab-width 8
      indent-tabs-mode t)
```