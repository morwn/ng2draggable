### draggable

[![Build Status](https://semaphoreapp.com/api/v1/projects/d4cca506-99be-44d2-b19e-176f36ec8cf1/128505/shields_badge.svg)](https://semaphoreapp.com/boennemann/badges)
[![Open Source Love](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://github.com/ellerbrock/open-source-badge/)

Angular 2 directive to make an element draggable. This is different from drag
and drop as this is used to drag a div around. [Live steve demo](https://cedvdb.github.io/ng2draggable/)

## Table of content
* [Installation](#installation)
* [Usage](#usage)
* [Images](#images)


## Install

Just copy draggable.directive.ts file content in a directive.


In any case you need to add the directive to your module.

## Usage

```
<div [ng2-draggable]="true"></div>
```

That's it! now your component can be moved around.

You can disable it as well :

```
<div [ng2-draggable]="boolean"></div>
```

The component will have a custom class added to it as well: `cursor-draggable`.
You can then use that css to costumize it :

```
/* Applies a grabbing hand on top of the div that's draggable*/
.cursor-draggable {
    cursor: grab;
    cursor: -moz-grab;
    cursor: -webkit-grab;
}
 /*  Apply a "closed-hand" cursor during drag operation. */
.cursor-draggable:active {
    cursor: grabbing;
    cursor: -moz-grabbing;
    cursor: -webkit-grabbing;
}
```
When the boolean input is false (it is true by default) the class is removed and
the component is no longer moveable.

## Images

If there is an image in the children of the dragged component, make sure to add the HTML5 property
draggable="false" to it. This property is used for drag and drop situations, and since ng2draggable directive
is not based on that property for various reasons, letting it in might make the component behave unexpectedly.


## Feedback

Your feedback is appreciated. If you wanna get involved you are welcome to.

You might be interested to follow me on twitter to be informed of future projects :) https://twitter.com/Ced_VDB
