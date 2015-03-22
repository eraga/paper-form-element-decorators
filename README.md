What this package does
=============================

Package provides a set of "Polymer paper" decorators for checkboxes, radios and other form elements in the way it does 
paper-input-decorator so they could still be submittable by the old form. 
  
It also provides a submit button decorator which submits the old form.  

Decorators extend corresponding paper elements and inherit all attributes/behaviour of their ancestors.

There is no decorators for all kinds of text inputs as there is already [paper-input-decorator](https://www.polymer-project.org/0.5/docs/elements/paper-input-decorator.html).

## Installation

```bower install paper-form-element-decorators```

## Currently available decorators

* **paper-checkbox-decorator** for ``input[type=checkbox]`` 
* **paper-toggle-button-decorator** for ``input[type=checkbox]`` 
* **paper-radio-button-decorator** for ``input[type=radio]``
* **paper-submit-button-decorator** for ``button`` and ``input[type=submit]`` 

## Examples

Decorators supposed to embed inputs which are invisible for the user (though, they are still visible to the form as 
they are still in the light DOM) and used only to store the data of the form.

It is possible to include all decorators at once:
```html
<link rel="import" href="../../bower_components/paper-form-element-decorators/paper-form-element-decorators.html">
```

### Checkbox
```html
	<paper-checkbox-decorator label="Check me" checked>
		<input type="checkbox" checked/>
	</paper-checkbox-decorator>
```

### Toggle button
```html
	<paper-toggle-button-decorator label="Check me" checked>
		<input type="checkbox" name="check" value="1" checked/>
	</paper-toggle-button-decorator>
```

### Radio group
```html
  <paper-radio-group selected="English"> 
    <paper-radio-button-decorator  label="English">
      <input type="radio" name="language" value="en" checked="checked"/>
    </paper-radio-button-decorator>
    <paper-radio-button-decorator  label="Russian (Русский)">
      <input type="radio" name="language" value="ru"/>
    </paper-radio-button-decorator>
  </paper-radio-group>
```

### Submit button
```html
	<paper-submit-button-decorator>
		<button name="op" value="Save" type="submit">Save</button> Save
	</paper-submit-button-decorator>
```

or

```html
	<paper-submit-button-decorator>
		<input name="op" value="Save" type="submit"/> Save
	</paper-submit-button-decorator>
```

**It is important to synchronize states of paper elements and nested inputs** first time you construct the document. 
This means that if some input is checked, so must be its decorator.


## TODO decorators

* select
* multiselect
