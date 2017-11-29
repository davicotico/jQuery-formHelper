# How to use
### Populate Form

```javascript
var frmValues = '{"var1": "", "var2": ""}';
$("#myFormID").populateForm(frmValues);
```
#### Plugin 'checkInput'
We have a checkbox array:
```html
<label><input type="checkbox" name="nameCheckbox[]" value="1"> Option 1</label>
<label><input type="checkbox" name="nameCheckbox[]" value="2"> Option 2</label>
<label><input type="checkbox" name="nameCheckbox[]" value="3"> Option 3</label>
```

Check input checkbox with name "nameCheckbox" and values "1", "3" (Option 1 and Option 3)
```javascript
$('#myFormID').checkInput('nameCheckbox', ["1", "3"]);
```
### Plugin checkAll

We have a checkbox array:
```html
<label><input type="checkbox" name="nameCheckbox[]" value="1"> Option 1</label>
<label><input type="checkbox" name="nameCheckbox[]" value="2"> Option 2</label>
<label><input type="checkbox" name="nameCheckbox[]" value="3"> Option 3</label>
```

Check all input checkbox with name "nameCheckbox"
```javascript
$('#myFormID').checkAll('nameCheckbox', true); // for unchecked: Set false the last parameter
```
Check/Uncheck using another input checkbox
```html
<label><input type="checkbox" id="masterCheckbox"> Check All</label>
```
```javascript
$('#myFormID').checkAll('nameCheckbox', $("#masterCheckbox"));
```
### Chained selects
Chain input select and populate select with result ajax.
```javascript
$('#select1').chainSelect($('#select2'), 'http://yourdomain.com/app/post.php');
```
The response must be an array json:
```
[{"value": "1", "text": "Option 1"}, {"value": "2", "text": "Option 2"}, ...]
```
