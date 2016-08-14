---
layout: default
title: "µ('microTK')"
---

<a href="https://github.com/microTK/microTK"><img style="position: absolute; top: 0; right: 0; border: 0;" src="https://camo.githubusercontent.com/365986a132ccd6a44c23a9169022c0b5c890c387/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f72696768745f7265645f6161303030302e706e67" alt="Fork me on GitHub" data-canonical-src="https://s3.amazonaws.com/github/ribbons/forkme_right_red_aa0000.png"></a>

# Usage

## Edge Release

```html
<script src="//cdn.rawgit.com/microTK/microTK/master/dist/microTK.min.js"></script>
```

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
</script>
```



