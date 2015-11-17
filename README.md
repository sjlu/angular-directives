# Angular Directives

## Objectives

* A basic understanding of what Angular directives are and what they provide
* Usage of commonly used directives
* Where to find a list of provided directives

## What is a directive?

Directives are a way of binding behavior to the DOM through HTML. So instead of defining clicks and mouseovers with
Javascript or jQuery, you do it straight inside your HTML. For example:

You're probably already used to writing this in jQuery:

**HTML**
```
<div id="button">Button</div>
```

**JS**
```
$('#button').on('click', function() {
  alert('clicked')
})
```

But in Angular, the same functionality can be written like so:

**HTML**
```
<div ng-click="alert('clicked')">Button</div>
```

So that's cool, but you're probably asking yourself what the advantage is.

* 
