# 2. Getting Started
## 2.3 Multiple Cursors and Incremental Search

Use `Ctrl + D` to select the current word (word that text cursor is currently on), repeat to select the next occurrence of that word as well. This will automatically create multiple cursors at the end of each selection so that you can quickly change a bunch if words. 

`Alt + F3` will select every occurrence of the current word and make cursors at the end of each.

Column selection uses `Shift + RMB` or `MMB`. `Ctrl` to add to selection and `Alt` to subtract.

`Shift + Ctrl + L` to add a cursor to the end of each line selected (so will yield multiple cursors if multiple lines are selected). Cursor is actually added to the end of the selection, so if the last line is only partially selected, the cursor won't be at the end of that line but at the end of the selection.

Instant search using `Ctrl + I` then press enter to go to that location.


## 2.4 The Command Palette

`Ctrl + Shift + P` to open the command palette, where you can search for and run any command (e.g. from the menu bar, etc). For example, if you type in `syntax javascript` you will find the command to change the syntax highlighting to Javascript. 

Note that this is fuzzy searching, that is it is matching the characters you type in order but they don't necessarily have to be sequential. For example, you could just type `stxjs` and it will find the set syntax to Javascript command.

Another example is you could type `sidebar` and find the command to toggle sidebar (plus you can see the keyboard shortcut here, `Ctrl + K + B`). 


## 2.5 Instant File Changing

`Ctrl + P` to open Goto Anything. This also fuzzy searches and so you can quickly find and open files (although only in the folder you have open).


## 2.6 Symbols

`Ctrl + R` to open Goto Symbol. This lets you quickly open things like classes. You can also use the Goto Anything dialogue and just type `@` to find these symbols. 

You can also combine opening a file along with a symbol by matching a file name and then typing `@` to match a symbol.


## 2.7 Key Bindings

Key bindings are set through a configuration file that is just a Javascript object. You can see the default key bindings in the default keymap file (which is overwritten each new version) and set your custom ones in the user keymap file. This allows you to easily search for the existing key bindings and modify them.