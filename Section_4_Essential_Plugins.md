# 4. Essential Plugins
## 4.1 Zen Coding

Note: Zen Coding has be superseded by Emmet and so this section of the notes uses Emmet but otherwise follows the lesson.

If your syntax is set to HTML, we can create nested HTML. For example if we type `ul>li*4` and then hit `Tab` we get
```html
<ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>
```
and we can hit tab to go into each `<li>` item.

Another example is `.container>.header+.main+.footer` which gives
```html
<div class="container">
    <div class="header"></div>
    <div class="main"></div>
    <div class="footer"></div>
</div>
```

`>` gives a child, `+` gives a sibling and `div.header` will give a `<div>` tag with a class of `header`. If we omit the `div`, Emmet will automatically place the appropriate tag which would often be a `<div>`.

Using `#` instead of `.` will give us an `id` rather than a class. `*` gives us multiple elements.

Note that the text cursor has to be at the end of the text for this to work. If we want to assign an attribute, we can do this by enclosing it in `[]`. For example `a.button[href=#]` gives
```html
<a href="#" class="button"></a>
```

If we wish to set text within tags, we use `{}`. `li{test}` gives
```html
<li>test</li>
```

We can also combine all of this into a more complicated expression. For example doing `ul>li*4[href=#]{Some Link}` gives
```html
<ul>
    <li><a href="#">Some Link</a></li>
    <li><a href="#">Some Link</a></li>
    <li><a href="#">Some Link</a></li>
    <li><a href="#">Some Link</a></li>
</ul>
```

If we wish to add a sibling to this, we would need to wrap the whole thing in `()`. So as an example, we might do `.container>(.header>header>h1{My Website})+.main+.footer>footer` which gives
```html
<div class="container">
    <div class="header">
        <header>
            <h1>My Website</h1>
        </header>
    </div>
    <div class="main"></div>
    <div class="footer">
        <footer></footer>
    </div>
</div>
```


## 4.2 Emmet 

We can also use Emmet shortcuts for CSS. For example, if we were to type `p20` and `Tab` it will expand to `padding: 20px;`. `m10` gives `margin: 10px;`. 

If you want a percentage, you can do `w80p` which gives `width: 80%;`. `m10-20` gives `margin: 10px 20px;`. `m0-auto` gives `margin: 0 auto;`.

If we need to do prefixes, we can use a `-`. For example, `-transition` gives
```CSS
-webkit-transition: ;
-o-transition: ;
transition: ;
```

We can also use `^` to go back a level when creating HTML and so if we were to do `header>h1^.main` we would get
```html
<header>
    <h1></h1>
</header>
<div class="main"></div>
```

We can also use it to generate Lorem text via `lorem20` which will generate 20 words of Lorem text.


## 4.5 Lightning Fast Folder and File Creation

Using the Advanced New File plugin, we can use `CTRL + ALT + N` to create a new file with a prompt to enter the filename. We can also use this to create a file in a directory and the plugin will automatically create any directories that do not exist.


## 4.6 Sidebar Enhancements

We can use the Sidebar Enhancements plugin to add more options for the sidebar such as adding an option to open a file in your default browser. 

We can also use this plugin to make the file open via a web server (E.g. via localhost). To do this, we need to have a project and we can then add 
```javascript
"url": "http://localhost:8888/"
```
for example and now when we open a file in our browser it will use that URL.


## 4.7 Sublime Linter

We can use the SublimeLinter plugin to add linting to Sublime. This plugin has been updated since the course has been made however, and we also need to install the actual lint plugins separately and these often need you to install separate binaries or libraries. See the documentation at [http://www.sublimelinter.com/en/latest/#user-documentation](http://www.sublimelinter.com/en/latest/#user-documentation) for more info.