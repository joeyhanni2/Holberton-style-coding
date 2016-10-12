By default, `emacs` will use spaces to indent your C code.

Of course, you don't want that.

In order to customise your `Emacs` configuration, you'll need to modify the file `.emacs` in your home directory. If this file does not already exist, you just need to create it.

**Don't put anything in your `.emacs` you don't understand!**

To tell emacs to use `tabs` instead, you just need to put the following lines in your `.emacs`:

```Emacs
(setq c-default-style "bsd"
      c-basic-offset 8
      tab-width 8
      indent-tabs-mode t)
```

Here, the size of a `tab` character in Emacs is set to `8`, so Emacs will display 8 spaces on your screen to represent a single `tab`. You can modify this value, to put a smaller one if you want, but just keep in mind that it's a good habit to keep an indentation of 8 columns: it makes your code more readable.

___

If you want to highlight lines exceeding 80 characters and trailing whitespace, you can add this to your `~/.emacs`:

```Emacs
(require 'whitespace)
(setq whitespace-style '(face empty lines-tail trailing))
(global-whitespace-mode t)
```

___


You should also add this line to your `~/.emacs`, if you want the current column along with the line in Emacs:

```Emacs
(setq column-number-mode t)
```