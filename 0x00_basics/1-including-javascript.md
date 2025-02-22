# Adding JavaScript to HTML

There are two primary ways to include JavaScript in an HTML document:

## 1. Internal JavaScript  
This method involves writing JavaScript directly inside a `<script>` tag within the HTML file.

### Example:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adding JavaScript by the Internal JavaScript method</title>
</head>
<body>
    <h1>JavaScript Example</h1>
    <script>
        console.log("Welcome to JavaScript.");
        console.log("JavaScript enhances web interactivity.");
    </script>
</body>
</html>
```

### Best Practice:
Placing the `<script>` tag before the closing `</body>` tag ensures that the HTML content loads first, preventing performance issues caused by JavaScript blocking page rendering.

## 2. External JavaScript  
With this approach, JavaScript is written in a separate `.js` file and linked to the HTML document using the `<script>` tag with the `src` attribute.

### Example:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>External JavaScript</title>
    <script src="script.js" defer></script>
</head>
<body>
    <h1>External JavaScript File</h1>
</body>
</html>
```

**script.js:**
```javascript
console.log("This is an external JavaScript file.");
console.log("Using external files keeps code modular and maintainable.");
```

## Optimizing JavaScript Loading  
JavaScript execution can delay page rendering, especially when the browser encounters a `<script>` tag during parsing. To improve performance, use the following strategies:

### 1. Using the `defer` Attribute  
- Ensures scripts are loaded only after the HTML document has been fully parsed.
- Preserves execution order of scripts.

**Example:**
```html
<script src="script.js" defer></script>
```

### 2. Using the `async` Attribute  
- Loads scripts asynchronously, meaning JavaScript downloads in parallel with HTML parsing.
- May execute scripts out of order if multiple scripts are loaded asynchronously.

**Example:**
```html
<script src="script.js" async></script>
```

### 3. Placing `<script>` at the End of `<body>`  
- Ensures all HTML content loads before JavaScript execution, reducing render-blocking.

**Example:**
```html
<body>
    ...
    <script src="script.js"></script>
</body>
</html>
```

## When to Use `defer` vs. `async`
| Attribute | Execution Order | Best Use Case |
|-----------|---------------|---------------|
| `defer`   | Executes after HTML parsing in order | Recommended for scripts that depend on DOM elements |
| `async`   | Executes as soon as downloaded, possibly out of order | Suitable for independent scripts like analytics |

### Additional Considerations
- **Minify JavaScript** files to reduce load time.
- **Use Content Delivery Networks (CDNs)** for faster script delivery.
- **Lazy load non-essential scripts** for better performance.

By applying these strategies, JavaScript can be efficiently included without hindering webpage performance.

