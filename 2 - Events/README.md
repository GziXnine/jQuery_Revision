# jQuery Events

jQuery provides a simple way to handle events in JavaScript. This document covers various types of events you can work with, including click, mouse events, keyboard events, and form events, along with some advanced features.

## Basic Events

### 1. Click Event

The click event is triggered when an element is clicked.

```javascript
$(() => {
  $("button").click(function () {
    $(this).css("color", "green"); // Change color of the clicked button
    $("button").css("background-color", "blue"); // Change background color of all buttons
    $("button").css("color", "white"); // Change text color of all buttons
  });
});
```

### 2. Double Click Event
The double-click event is triggered when an element is double-clicked.

```javascript
$(() => {
  $("button").dblclick(function () {
    $("p").css("color", "green"); // Change the color of a paragraph to green
    $(this).css("color", "green"); // Change the color of the clicked button
    $("button").hide(); // Hide the button
  });
});
```
### 3. Mouse Enter and Mouse Leave Events
These events trigger when the mouse enters or leaves an element.

```javascript
$(() => {
  $("button").mouseenter(function () {
    $(this).css("color", "red"); // Change color to red when mouse enters
  });

  $("button").mouseleave(function () {
    $(this).css("color", "green"); // Change color to green when mouse leaves
  });
});
```
### 4. Hover Event
The hover event can take two functions: one for mouse enter and one for mouse leave.

```javascript
$(() => {
  $("button").hover(
    function () {
      $(this).css("color", "orange"); // Change color to orange on hover
    },
    function () {
      $(this).css("color", "yellow"); // Change color to yellow when not hovering
    }
  );
});
```
---

## Event Binding
### 1. Bind Method
The bind method attaches event handlers to elements.

```javascript
$(() => {
  $("button").bind("click", function () {
    alert("Button clicked!");
  });
});
```

### 2. Multiple Events
You can bind multiple events at once.

```javascript
$(() => {
  $("button").bind("click mouseover", function () {
    alert("Button clicked or mouseover!");
  });
});
```

### 3. Event Map
Using an event map allows you to bind multiple events with different handlers.

```javascript
$(() => {
  $("button").bind({
    click: function () {
      alert("Button clicked!");
    },
    mouseover: function () {
      alert("Mouse is over the button!");
    },
  });
});
```
---

## Live and Delegate Events
### 1. Live Method (Deprecated)
The live method binds events to elements that may be added in the future. However, it's deprecated in recent jQuery versions.

```javascript
$(() => {
  $("button").live("click", function () {
    alert("Button clicked!");
  });
});
```

### 2. Delegate Method
The delegate method allows you to attach event handlers to a parent element, which then affects its child elements.

```javascript
$(() => {
  $("div").delegate("button", "click", function () {
    alert("Delegate: Button clicked!");
  });
});
```
---

## On Method
The on method is more versatile than bind, and it supports several features.

### 1. Basic Usage
```javascript
$(() => {
  $("button").on("click", function () {
    alert("Button clicked!");
  });
});
```

### 2. Multiple Events
You can also bind multiple events using on.

```javascript
$(() => {
  $("button").on("click mouseover", function () {
    alert("Button clicked or mouseover!");
  });
});
```

### 3. Event Data
You can pass additional data when the event is triggered.

```javascript
$(() => {
  $("button").on("click", { name: "Ahmed" }, function (e) {
    alert("Hello, " + e.data.name);
  });
});
```

### 4. Custom Events
You can create and trigger custom events.

```javascript
$(() => {
  $(".custom").on("myCustom", function (event, myHeight, myWidth) {
    $(this).css({
      height: myHeight,
      width: myWidth,
      backgroundColor: "black",
    });
  });

  $("button").on("click", () => {
    $(".custom").trigger("myCustom", ["300px", "300px"]); // Trigger custom event
  });
});
```
---

## Prevent Default Behavior
Preventing the default action of an event can be useful, especially for links and form submissions.

```javascript
$(() => {
  $("a").click(function (e) {
    e.preventDefault(); // Prevent default action (navigation)
    alert("Link clicked, but navigation prevented!");
  });
});
```
---

## Keyboard Events
You can listen for keyboard events like keydown, keypress, and keyup.

```javascript
$(() => {
  $("input").keydown(function () {
    alert("Key down event triggered!");
  });

  $("input").keypress(function () {
    alert("Key press event triggered!");
  });

  $("input").keyup(function () {
    alert("Key up event triggered!");
  });
});
```
---

## Form Events
### 1. Change Event
Triggered when the value of an input changes.

```javascript
$(() => {
  $("input").change(function () {
    alert("Input value changed!");
  });
});
```

### 2. Focus and Blur Events
Triggered when an input gains or loses focus.

```javascript
$(() => {
  $("input").focus(function () {
    $(this).css("background", "yellow"); // Highlight input on focus
  });

  $("input").blur(function () {
    $(this).css("background", "white"); // Reset background on blur
  });
});
```
---

## One-Time Event Handling
Using the one method allows an event to be triggered only once.

```javascript
$(() => {
  $("input").one("click", function () {
    alert("This will only show once!");
  });
});
```
---

## Window Events
### 1. Resize Event
Triggered when the window is resized.

```javascript
$(() => {
  $(window).resize(function () {
    $("span").text("Window resized!");
  });
});
```

### 2. Mouse Movement Tracking
You can track mouse movement on the document.

```javascript
$(() => {
  $(document).mousemove(function (event) {
    $("span").text("X: " + event.pageX + ", Y: " + event.pageY);
  });
});
```
---

## Form Submission
You can intercept form submission and perform custom actions.

```javascript
$(() => {
  $("form").submit(function (event) {
    event.preventDefault(); // Prevent default submission
    alert("Form submitted!");
  });
});
```
--- 

### Explanation 🎯
- **Section Headers**: Each section has a clear header to define what types of events are being discussed.
- **Code Snippets**: The code examples are structured clearly with comments explaining the purpose of each line.
- **Usage**: Each section describes how to use the event in a practical context, making it easier to understand.
- **Conclusion**: Summarizes the document and reinforces the importance of event handling in jQuery.

Feel free to play around with the examples to see how these events work in practice!
