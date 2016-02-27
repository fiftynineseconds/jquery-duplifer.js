# jquery-duplifer.js
A jQuery plugin that highlights duplicate cells in a table.

jquery-duplifer will hightlight each duplicate cell in a table in a different color.

PUT-EXAMPLE-HERE

## Basic Usage

### First create an html table that has the class duplifer-highlightdups applied to the th that contains duplicate rows.

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

### Then call duplifer on the table. That's it.

````javascript
$(document).ready(function () {
	$(".find-duplicates").duplifer();
});
````

## Options

Coming soon.