# element-xpath

Javascript library and jQuery plugin for determining the XPath of an HTML DOM element.

## Usage with jQuery (jquery.element-xpath.js)

```javascript
$(element).elementXPath(options);
```

Example:

```html
<head>
	<script src="jquery.min.js"></script>
	<script src="jquery.element-xpath.min.js"></script>
</head>
<body>
	<div id="wrapper">
		<div id="content">
			<div id="sidebar">
				get the path of this!
			</div>
		</div>
	</div>
</body>
```

```javascript
$("#sidebar").elementXPath();
// returns: html//body//div[@id='wrapper']//div[@id='content']//div[@id='sidebar']
```

## Usage alone (element-xpath.js)

```javascript
ElementXPath(element, options);
```

Example:

```html
<head>
	<script src="element-xpath.min.js"></script>
</head>
<body>
	<div id="wrapper">
		<div id="content">
			<div id="sidebar">
				get the path of this!
			</div>
		</div>
	</div>
</body>
```

```javascript
ElementXPath(document.getElementById("sidebar"));
// returns: html//body//div[@id='wrapper']//div[@id='content']//div[@id='sidebar']
```

## Options
Customize the functionality with the following options:

### `unique` (default: `false`)
A boolean, if true, path contains a unique route to the element.

### `directDescendant` (default: `false`)
A boolean, if true, path contains the direct descendant operator (/) for all the elements.

### `startWithClosestID` (default: `false`)
A boolean, if true, path begins with the first element with an ID up the ancestor tree. E.g. `html//body//div[@id='wrapper']//div[@id='content']//div[@id='sidebar']//ul//li//a` would be shortened to `div[@id='sidebar']//ul//li//a`.


## Browser Support

* IE 5.5+
* Chrome
* Firefox
* Safari
* Opera

## License

Distributed under the MIT license.