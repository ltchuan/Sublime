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