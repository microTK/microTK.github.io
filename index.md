---
layout: default
title: "µ('microTK')"
---

# Why Use microTK?

It is tiny!  The current minified version is under 5k, while most of the other popular libraries are well over 80k. It is perfect for those times when you just don't need the power of larger libraries. 

* * *

# Usage

## Edge Release

```html
<script src="//cdn.rawgit.com/microTK/microTK/master/dist/microTK.min.js"></script>
```

[![Build Status](https://drone.io/github.com/thenderson21/microTK/status.png)](https://drone.io/github.com/thenderson21/microTK/latest)

## Latest Release ({{site.version}})

```html
<script src="//cdn.rawgit.com/microTK/microTK/{{site.version}}/dist/microTK.min.js"></script>
```

## Example

```html
<script src="//cdn.rawgit.com/microTK/microTK/master/dist/microTK.min.js"></script>

<script>
 var µMenu= µ(".menu"); // or microTk(".menu")

 //prints each element to console.
 µMenu.each(function(element){
     console.Loge(element);
 });

 //Chainable
 µMenu.addClass('sample').addEvent('click', function(e){
            //toggles the 'active' class
            µMenu.toggleClass("active");
        });


 //Individual HTMLElement(s)
 µMenu[0].classlist.remove("active");

 //or
 
 µ(µMenu[0]).addAttribute("title", "First");
</script>
```

* * *

# What if microTK doesn't do something I need?

Extend it!  MicroTK is fully extendable. A basic plugin might look like:

```javascript
 MicroTK.prototype.data = function(name, value) {
      var _element, i, len;
      for (i = 0, len = this.length; i < len; i++) {
        _element = this[i];
        _element.setAttribute('data-' + name, value);
      }
      return this;  
    };

```

 or in CoffeeScript

```coffeescript
 MicroTK::data = ((name, value) ->
        for _element in @
            _element.setAttribute 'data-' + name, value
        this
```

* * *

# License

 MicroTk is released under the [MIT](https://github.com/microTK/microTK/blob/master/LICENSE) license.

