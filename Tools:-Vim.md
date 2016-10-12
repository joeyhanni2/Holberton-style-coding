If you are a `vim` user and you want to customise tabs and indentation, just read the following guide.

In order to customise your `vim` configuration, you'll need to modify the file `.vimrc` in your home directory. If this file does not already exist, you just need to create it.

**Don't put anything in your `.vimrc` you don't understand!**

#### Tabs

To customise tabs length, you can add the following line to your `~/.vimrc`:

```VimL
set tabstop=8 shiftwidth=8
```

Here, the size of a tab character in Vim is set to 8, so Vim will display 8 spaces on your screen to represent a single tab. You can modify this value, to put a smaller one if you want, but just keep in mind that it's a good habit to keep an indentation of 8 columns: it makes your code more readable.

___

#### Indentation

To indent automatically a line depending on the previous one when you hit `Enter`, just add the following line to your `.vimrc`:

```VimL
set autoindent
```

You can also use intelligent indentation for C code with `Vim`:

```VimL
set smartindent
set cindent
```

___

#### Extras

You can enable syntax highlighting in `Vim` by adding the following rule in your `.vimrc`:

```VimL
syntax enable
```

You can display the current line and column in `Vim` with the following rule:

```VimL
set number
```