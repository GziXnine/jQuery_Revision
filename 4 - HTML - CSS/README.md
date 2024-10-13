# HTML / CSS in jQuery 📄✨

## 1. Get and Set Methods
### Description
These methods are used to retrieve and manipulate HTML attributes, text, and values of elements.

- `attr()`: Get or set attributes of an element.
- `text()`: Get or set the text content of an element.
- `html()`: Get or set the HTML content of an element.
- `val()`: Get or set the value of form elements.

### Example
```javascript
$(() => {
  $("button").click(() => {
    console.log($("div").html()); // [1] Get
    $("div").html("<h1>Hello World</h1>"); // [2] Set
  });
});
```
Difference Between `text()` and `html()`
`text(`): Retrieves or sets the text content, stripping away any HTML tags.
`html()`: Retrieves or sets the HTML content, preserving any HTML tags.

## 2. Manipulation Methods
### Description
Methods to manipulate elements in the DOM by adding, removing, or modifying content.

- `append()`: Insert content at the end of selected elements.
- `appendTo()`: Insert selected elements at the end of specified target elements.
- `prepend()`: Insert content at the beginning of selected elements.
- `prependTo()`: Insert selected elements at the beginning of specified target elements.
- `after()`: Insert content after the selected elements.
- `before()`: Insert content before the selected elements.
  
### Example
```javascript
$(() => {
  $("button").click(() => {
    $("div").before("<h1>Hello World</h1>"); // [6] before()
  });
});
```

## 3. Removal Methods
### Description
Methods to remove elements or their contents from the DOM.

- `remove()`: Remove the selected element and its children from the document.
- `empty()`: Remove all child elements from the selected element.

### Example
```javascript
$(() => {
  $("button").click(() => {
    $("div").remove(".jQuery"); // More accurate, removes div.jQuery
    $("div").empty(); // [2] empty()
  });
});
```

## 4. CSS Class Manipulation
### Description
Methods for managing CSS classes on elements.

- `addClass()`: Add a class to the selected elements.
- `removeClass()`: Remove a class from the selected elements.
- `toggleClass()`: Toggle a class on the selected elements.
- `css()`: Get or set the CSS properties of the selected elements.

### Example
```javascript
$(() => {
  $("button").click(() => {
    $("div").toggleClass("jQuery"); // [3] toggleClass()
  });
});
```

## 5. CSS - Get / Set
### Description
Methods for getting and setting CSS properties.

### Example
```javascript
$(() => {
  $("button").click(() => {
    $("div").css({
      color: "red",
      fontSize: "30px",
    }); // Set multiple CSS properties
  });
});
```

## 6. Dimensions
### Description
Methods for retrieving the dimensions of elements.

- `width()`: Get or set the width of an element.
- `height()`: Get or set the height of an element.
- `innerWidth()`: Get the width of an element, including padding.
- `innerHeight()`: Get the height of an element, including padding.
- `outerWidth()`: Get the width of an element, including padding and border. Use `true` to include margin.
- `outerHeight()`: Get the height of an element, including padding and border. Use` true` to include margin.
 
## 7. Clone and Detach
### Description
Methods for cloning and detaching elements in the DOM.

- `clone()`: Creates a copy of the selected elements.
- `detach()`: Removes the selected elements while keeping all data and events associated with them.

### Example
```javascript
$(() => {
  $("button").click(function () {
    $("div").clone().appendTo("body"); // Clone and append to body
  });
});
```

## 8. Offset and Position
### Description
Methods for getting the position of elements in the document.

- `offset()`: Get the current position of an element relative to the document.
- `position()`: Get the current position of the first element relative to its offset parent.
  
### Example
```javascript
$(() => {
  $("button").click(function () {
    var x = $("p").offset();
    alert("Top: " + x.top + " Left: " + x.left); // Get offset position
  });
});
```

## 9. prop() vs. attr()
### Description
- `prop()`: Get or set the property of an element.
- `attr()`: Get or set the attribute of an element.

### Example
```javascript
$(() => {
  $("button").click(function () {
    alert($("#test").prop("href")); // Get the href property of an element
  });
});
```

## 10. replaceWith
### Description
Replace the selected element with new content.

### Example
```javascript
$(() => {
  $("h1").replaceWith("<h2>Replaced</h2>"); // Replace h1 with h2
});
```

## 11. Scroll
### Description
Methods for retrieving the scroll position of the window.

### Example
```javascript
$(() => {
  $(window).scroll(() => {
    console.log($(window).scrollTop()); // Get vertical scroll position
    console.log($(window).scrollLeft()); // Get horizontal scroll position
  });
});
```

## 12. Wrap and Unwrap
### Description
Methods for wrapping elements with new HTML or removing wrapping elements.

- `wrap()`: Wraps the selected elements with the specified HTML.
- `wrapAll()`: Wraps all selected elements in a single HTML structure.
- `wrapInner()`: Wraps the inner content of the selected elements with the specified HTML.
- `unwrap()`: Removes the parent element of the selected elements.
  
### Example
```javascript
$(() => {
  $("h1").wrap("<div></div>"); // Wrap h1 with a div
  $("h1").unwrap(); // Remove the wrapping div
});
```

# Conclusion 🎉
In this section, we've explored the powerful features of jQuery that enhance HTML and CSS manipulation. From basic tasks like modifying text and adding classes to advanced techniques such as cloning elements and handling events, jQuery simplifies complex operations, making our code cleaner and more efficient.

Remember, mastering these jQuery methods not only improves your development speed but also enhances user experience through dynamic and responsive design. Keep practicing these concepts to build interactive and engaging web applications! **Happy coding!** 💻✨