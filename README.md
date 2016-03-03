# jquery-duplifer.js
A jQuery plugin that highlights duplicate cells in a table using a randomly-generated (visually pleasing) color by default. You may also use your own color generator.

jquery-duplifer will hightlight each duplicate cell in a table in a different color.

![Example Table](https://github.com/fiftynineseconds/jquery-duplifer.js/blob/master/table-example.png)

## Basic Usage

First create an html table that has the class duplifer-highlightdups applied to the th that contains duplicate rows.

```html
<table class="find-duplicates">
		<thead>
			<tr>
				<th>Column 1</th>
				<th>Column 2</th>
				<th class="duplifer-highlightdups">Column 3</th>
			</tr>
		</thead>

		<tbody>
			<tr>
				<td>Test 1</td>
				<td>Test 2</td>
				<td>Test 3</td>
			</tr>

			<tr>
				<td>Test 1</td>
				<td>Test 2</td>
				<td>Test 2</td>
			</tr>

			<tr>
				<td>Test 1</td>
				<td>Test 1</td>
				<td>Test 1</td>
			</tr>

			<tr>
				<td>Test 3</td>
				<td>Test 3</td>
				<td>Test 2</td>
			</tr>

			<tr>
				<td>Test 1</td>
				<td>Test 2</td>
				<td>Test 3</td>
			</tr>

			<tr>
				<td>Test 1</td>
				<td>Test 2</td>
				<td>Test 3</td>
			</tr>
		</tbody>
	</table>
```

Then call duplifer on the table. That's it.

````javascript
$(document).ready(function () {
	$(".find-duplicates").duplifer();
});
````

## Options

There are two optional parameters.

### colorGenerator

Method to determine the colors that are generated. 

Parameter `index` is the zero-based index of the found duplicate. The first duplicate found is index 0, the second is 1...

By default the colors are randomly generated.

```javascript
$(".find-duplicates").duplifer({
	colorGenerator: function(index){
    	var colors = ["red", "orange", "yellow", "green", "blue", "indigo", "violet"];
		return colors[index];
    }
});
```

### highlightClass

Specifies the class name of the th that contains the column to highlight. By default it is `duplifer-highlightdups`

```javascript
$(".find-duplicates").duplifer({
	highlightClass: "myClassName"
});
```


