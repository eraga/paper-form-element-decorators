# paper-form-element-decorators
Decorate à la Material Design checkboxes, radios and other form elements in the way it does paper-input-decorator so 
they could still be submittable by form.  

Decorators extend corresponding paper elements inheriting all attributes and behaviour of their ancestors.

# Currently available decorators

* **paper-checkbox-decorator** for ``input[type=checkbox]`` 
* **paper-toggle-button-decorator** for ``input[type=checkbox]`` 
* **paper-radio-button-decorator** for ``input[type=radio]``
* **paper-submit-button-decorator** for ``button`` and ``input[type=submit]`` 

# Example

```
  <paper-checkbox-decorator label="Check me" checked>
    <input type="checkbox" checked/>
  </paper-checkbox-decorator>
```      

**It is important to synchronize states of paper elements and nested inputs** first time you construct the document. 
This means that if some input is checked, so must be its decorator. 

# TODO elements

* select
