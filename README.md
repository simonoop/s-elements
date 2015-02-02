# s-elements
angular elements 
A simple angular directive to create a button group. Doesn't need bootstrap.

# why?
I needed a quick & dirty angular directive to create a button group and I couldn't find a simple one.
I'm <b>pretty</b> sure I'm reinventing the wheel for the 1000th time and there's probably a better implementation out there but, hey!, it works or so it seems! :)

# demo
* <a href='http://plnkr.co/rGVZjeryxFfSyyfojiAA'>Plunker demo</a>

# usage

* You'll need angular 
* Copy ng.s-elements.js, ng.s-elements.css and sbuttons.html to a folder, ex: /s-elements/
* Add the js and the css file to your page:
```html
<script type="text/javascript" src="/s-elements/ng.s-elements.js"></script>
<link rel="stylesheet" href="/s-elements/ng.s-elements.css"/>
```
* Edit /s-elements/ng.s-elements.js and change the templatePath like so:
```javascript
var settings = {
    templatePath : '/s-elements/'
}
```
* Inject it into your app:
```javascript
var app = angular.module("app",['s-elements'])
```
* Add an <i>sbuttons</i> tag to create a simple array driven button group:
```html
<sbuttons label="So, what do you say?" default="yes" options="['yes','no']" model="answer"></sbuttons> 
```
* That's it. The previous example will create a two button group "yes" and "no". The default (optional) will be "yes" and the model will be "answer". It'll also add a (optional) label.
* You can use an object as the options source but you'll have to add a key and a text attribute so it knows what to do:
```html
<sbuttons default="2" options="[{id:1,name:'Apple'},{id:2,name:'Sony'}" model="brand_id" key="id" text="name"></sbuttons> 
```

# what?
Yeap. Pretty simple and naive. Probably breaking a "few" good practices too.
