---
layout: default
title: "µ('microTK')"
---

# Usage

```html
<script src="microTK.min.js"></script>

<script>
 var µMenu= µ(".menu"); // or microTk(".menu")

 //toggles the 'active' class
 µMenu.toggleClass("active");

 //prints each element to console.
 µMenu.each(function(element){
     console.Loge(element);
 });

 //Chainable
 µMenu.addClass('sample').addEvent('click', function(e){
            //NOTE: all action pass the HTMLElement not the MicroTK object.
            µ(e).removeClass('sample');
        });
</script>
```



