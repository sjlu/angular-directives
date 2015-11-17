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

The advantage of using directives is that your events are now closly wound into your HTML, making it easier to read and figure out what the element does even in your Chrome inspector. Development and debugging is now a tad bit easier.

Lets take this one step further, lets say we want to call a function that we explicitly defined. Well, its as easy as just calling it as long it is on the `$scope`.

**HTML**
```
<div ng-click="myClickHandler()"></div>
```

**JS**
```
angular.controller('myController', function($scope) {
  $scope.myClickHandler = function() {
    alert('myClickHandler')
  }
})
```

## Some common directives

Now that you know what directives are, Angular has some that are built in. Here are some common ones that you'll most likely come across.

### ng-click, ng-focus, ng-mouseover

These are self-explanitory. As a user clicks, focuses, or mousesover, perform the necessary directive function.

**HTML**
```
<div ng-mouseover="console.log('mouseover')"></div>
```

### ng-hide, ng-show, ng-if

These directives can help you show or hide elements based on the boolean value specified inside the directive.

**HTML**
```
<div ng-show="myBooleanVariable"></div>
```

### ng-repeat


