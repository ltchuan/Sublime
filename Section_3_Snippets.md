# 3. Snippets
## 3.1 Your First Snippet

You can see what snippets you have via `Tools -> Snippets` but this just opens the Command Palette with the word 'Snippet:' already typed in. This shows the snippets associated with the current file type. You can enter the snippets like this but also see the shortcut for each snippet here.

For example, if you type `fun` and then hit `Tab` with the syntax set to Javascript, you would get
```javascript
function function_name(argument) {
    // body...
}
```
This also has tab insertion, and so it starts with the `function_name` selected and if you hit tab, it will then go to the argument and then the body.

You can create a new snippet via `Tools -> Developer -> New Snippet` (it doesn't appear to be in the Command Palette for some reason).

This will give
```xml
<snippet>
    <content><![CDATA[
Hello, ${1:this} is a ${2:snippet}.
]]></content>
    <!-- Optional: Set a tabTrigger to define how to trigger the snippet -->
    <!-- <tabTrigger>hello</tabTrigger> -->
    <!-- Optional: Set a scope to limit where the snippet will trigger -->
    <!-- <scope>source.python</scope> -->
</snippet>
```
The main area you want to edit is the `Hello, ${1:this} is a ${2:snippet}.` which will modify what the snippet expands into.

You can also uncomment the `<!-- <tabTrigger>hello</tabTrigger> -->` via `Ctrl + /` (this toggles commenting) and set the tab trigger.

The snippet should be saved in `Packages\User` and needs to be saved with the extension `.sublime-snippet`. If you save it in a folder with a language name, Sublime will automatically limit the scope to that language (e.g. saving to a folder `Javascript` will limit its scope to Javascript).

The tab stops in the snippet are set via the `${...}` syntax in the earlier example. In that example, we have `${1:this}`, which indicates that is the position of the first tab stop and has the default value of `this`.

The name of the snippet name is set by the file name of the snippet so giving clear file names for the snippets is important.