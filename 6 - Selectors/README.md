# 🎯 Selectors in jQuery 🎯

Selectors are powerful tools in jQuery that allow you to target specific elements in the DOM for manipulation. Whether you're working with basic or advanced selectors, mastering them will enhance your web development skills! 🚀

## 📚 1. Basic Selectors

### 1. Universal Selector `*`
Selects all elements.
```javascript
$("*").css("color", "blue"); // Change text color to blue for all elements
```

### 2. ID Selector `#id`
Selects an element by its ID.
```javascript
$("#header").css("background", "yellow"); // Change the background color of the element with id="header"
```

### 3. Class Selector `.class`
Selects elements with a specific class.
```javascript
$(".highlight").css("font-weight", "bold"); // Make all elements with class "highlight" bold
```

### 4. Element Selector
Selects elements by their tag name.
```javascript
$("p").css("font-size", "18px"); // Change the font size of all <p> elements
```
### 5. Grouping Selector `element, element`
Selects multiple elements.
```javascript
$("h1, h2").css("color", "red"); // Change color to red for all <h1> and <h2> elements
```

### 6. Descendant Selector `element element`
Selects elements that are descendants of a specified element.
```javascript
$("div p").css("margin", "10px"); // Select all <p> inside <div> and set margin
```

### 7. Child Selector `element > element`
Selects direct children of a specified element.
```javascript
$("ul > li").css("list-style-type", "circle"); // Set list style for direct <li> children of <ul>
```

### 8. Adjacent Sibling Selector `element + element`
Selects the next sibling of a specified element.
```javascript
$("h1 + p").css("font-style", "italic"); // Style the first <p> that follows an <h1>
```

### 9. General Sibling Selector `element ~ element`
Selects all siblings after the specified element.
```javascript
$("h1 ~ p").css("color", "green"); // Change color of all <p> siblings after <h1>
```

## ⚡ 2. Advanced Selectors
### 1. `:animated`
Selects elements that are currently being animated.

```javascript
console.log($(":animated")); // Log all currently animated elements
```

### 2. `eq(index)`
Selects the element at the specified index.
```javascript
console.log($("h1:eq(1)")); // Select the second <h1> element
```

### 3. `:even` / `:odd`
Selects even or odd indexed elements.

```javascript
console.log($("h1:even")); // Log all even <h1> elements
console.log($("h1:odd"));  // Log all odd <h1> elements
```

### 4. `:first` / `:last`
Selects the first or last element of a set.

```javascript
console.log($("h1:first")); // Log the first <h1> element
console.log($("h1:last"));  // Log the last <h1> element
```

## 🔎 3. Child and Sibling Selectors
### 1. `:first-child`
Selects the first child of its parent.
```javascript
$("p:first-child").css("font-weight", "bold"); // Bold the first <p> child
```

### 2. `:last-child`
Selects the last child of its parent.
```javascript
$("p:last-child").css("text-decoration", "underline"); // Underline the last <p> child
```

### 3. `:nth-child(n)`
Selects the nth child of its parent.

```javascript
$("li:nth-child(3)").css("color", "orange"); // Change the color of the third <li>
```

### 4. `:only-child`
Selects an element that is the only child of its parent.

```javascript
$("p:only-child").css("font-size", "24px"); // Change font size of only child <p>
```

## 💡 4. Attribute Selectors
### 1. Basic Attribute Selector
Selects elements with a specific attribute.
```javascript
$("[title]").css("border", "1px solid black"); // Add border to elements with title attribute
```

### 2. Attribute Equals Selector
Selects elements with a specific attribute value.
```javascript
$("a[href='Test']").css("color", "red"); // Change color for links with href='Test'
```

### 3. Attribute Not Equals Selector
Selects elements whose attribute value does not equal a specific value.
```javascript
$("a[href!='Test']").css("text-decoration", "none"); // Style links not pointing to 'Test'
```

### 4. Attribute Contains Selector
Selects elements whose attribute value contains a specific substring.
```javascript
$("a[href*='Link']").css("font-weight", "bold"); // Bold links containing 'Link'
```

### 5. Attribute Starts With Selector
Selects elements whose attribute value starts with a specific value.
```javascript
$("a[href^='Start']").css("color", "green"); // Change color for links starting with 'Start'
```

# 🚀 Conclusion
Selectors in jQuery are fundamental for navigating and manipulating the DOM efficiently. By mastering these basic and advanced selectors, you'll be equipped to build dynamic, interactive web applications! Keep practicing, and **happy coding!** 🎉