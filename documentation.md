---
layout: page
title: Documentation
author: Todd Henderson
---

## Contents
{:.no_toc}

* ToC
{:toc}

---

### microTK(selector, scope) 

Creates a new instance of MicroTK with specified query paremeters or element(s)

**Parameters**

**selector**: `string | HTMLElement`, The selector to be queried for or the HTMLElement(s) to be added.

**scope**: `HTMLElement`, The scope of the query selection.

**Returns**: `microTK`, An instance of the MicroTK object.

**Example**:

```js
var menu = µ("#menu");
```

********************

## Class: MicroTK
The main class of the microTK library, it is a list of selected HTMLElement 
that various actions be performed on.

### MicroTK.addAttribute(name, value) 

Adds an attribute to the selected elements.

**Parameters**

**name**: `string`, The attribute to be added.

**value**: `string`, The value of the attribute.

**Returns**: `MicroTK`, A copy of the MicroTK object.

**Example**:

```js
µ("#menu").addAttribute("title", "test");
```

****************

### MicroTK.addClass(className) 

Adds a class to the selected elements.

**Parameters**

**className**: `string`, The class to be added.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
µ("#menu").addClass("active");
```

********************

### MicroTK.addEvent(event, action) 

Adds an event to the selected elements.

**Parameters**

**event**: `string`, Event to be added.

**action**: `function`, Function to be run on event.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
µ("#menu").addEvent("click", function (e){
    µ(e).toggleClass("active");   
});
```

********************

### MicroTK.append(element) 

Appends an HTMLElement into the selected elements.

**Parameters**

**element**: `HTMLElement`, Element to be removed.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
var element = document.createElement("div")
µ("#menu").append(element);
```

********************

### MicroTK.each(action) 

Performs an action on the selected elements

**Parameters**

**action**: `elementAction`, Function to be run when the element has providec class.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
µ("#menu").each(function (e){
    e.classList.add("active");   
});
```

********************

### MicroTK.hasAttribute(name, action) 

Checks to see if elements contains provided class and performs provided action.

**Parameters**

**name**: `string`, The attribute to be added.

**action**: `elementAction`, Function to be run when the element has provided attribute.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
µ("#menu").hasAttribute("title", function (e){
    e.title = "woohoo"; 
});
```

********************

### MicroTK.hasClass(className, action) 

Checks to see ff elements contains provided class and performs provided action.

**Parameters**

**className**: `string`, Element to be tested for.

**action**: `elementAction`, Function to be run when the element has providec class.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
µ("#menu").hasClass("active", function (e){
    e.classList.remove("active");   
});
```

********************

### MicroTK.prepend(element) 

Prepends an HTMLElement into the selected elements.

**Parameters**

**element**: `HTMLElement`, Element to be removed.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
var element = document.createElement("div")
µ("#menu").prepend(element);
```

********************

### MicroTK.remove() 

Removes the selected elements from the DOM.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
µ("#menu").remove();
```

********************

### MicroTK.removeAttribute(name) 

Removes an attribute from the selected elements.

**Parameters**

**name**: `string`, The attribute to be added.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
µ("#menu").removeAttribute("id");
```

********************

### MicroTK.removeClass(className) 

Removes a class from the selected elements.

**Parameters**

**className**: `string`, Class to be removed.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
µ("#menu").removeClass("active");
```

********************

### MicroTK.toggleClass(className) 

Toggles a class in selected elements.

**Parameters**

**className**: `string`, Class to be toggled.

**Returns**: `microTK`, A copy of the MicroTK object.

**Example**:

```js
µ("#menu").toggleClass("active");
```