
# Boiled Page form component

Form SCSS component for Boiled Page frontend framework. It is intended to create different form elements, labels, tips, fieldsets, group form elements together.

## Install

Place `_form.scss` file to `/assets/css/components` directory, and add its path to components block in `assets/css/app.scss` file.

## Usage

### Form component

Form is intended to create a form that contains different form elements.

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`form` | Applies a form. | `<form class="form"></form>`

#### Examples

##### Example 1

The following example shows an empty form.

```html
<form class="form" method="post" action="#"></form>
```

### Form input component

Form input is intended to create input, select and textarea form elements.

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`form-input` | Applies a form input. | `<input class="form-input" />`
`form-input--select` | Adds select specific properties to form input. | `<select class="form-input form-input--select"></select>`
`form-input--textarea` | Adds textarea specific properties to form input. | `<textarea class="form-input form-input--textarea"></textarea>`

#### Examples

##### Example 1

The following example shows an input type form input.

```html
<input name="name" id="name" class="form-input" type="text" />
```

##### Example 2

The following example shows a select type form input.

```html
<select name="category" id="category" class="form-input form-input--select">
  <option value="">Choose category</option>
  <option value="manufacturing">Manufacturing</option>
  <option value="shipping">Shipping</option>
  <option value="administration">Administration</option>
  <option value="human-resources">Human Resources</option>
</select>
```

##### Example 3

The following example shows a textarea type form input.

```html
<textarea name="message" id="message" class="form-input form-input--textarea" rows="3"></textarea>
```

#### Extension ideas

##### Small form input

```scss
/* Form input component extensions */
input.form-input, select.form-input, textarea.form-input {

  // Small form input
  &.form-input--small {
    font-size: $small-font-size;
  }
}
```

##### Large form input

```scss
/* Form input component extensions */
input.form-input, select.form-input, textarea.form-input {

  // Large form input
  &.form-input--large {
    font-size: $large-font-size;
  }
}
```

### Form control component

Form control is intended to create radio, checkbox form elements.

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`form-control` | Applies a form control. | `<label class="form-control"></label>`
`form-control--checkbox` | Adds checkbox specific properties to form control. | `<label class="form-control form-control--checkbox"></label>`
`form-control--radio` | Adds radio specific properties to form control. | `<label class="form-control form-control--radio"></label>`
`form-control--switch` | Adds switch specific properties to form control. It is a checkbox styled as a switch. | `<label class="form-control form-control--switch"></label>`
`form-control-indicator` | Applies indicator of form control. | `<span class="form-control-indicator"></span>`

#### Examples

##### Example 1

The following example shows a checkbox form element.

```html
<label class="form-control form-control--checkbox">
  <input name="agreement" type="checkbox" />
  <span class="form-control-indicator"></span>
  I agree to the terms and conditions
</label>
```

##### Example 2

The following example shows a radio form element.

```html
<label class="form-control form-control--radio">
  <input name="gender" type="radio" value="male" />
  <span class="form-control-indicator"></span>
  Male
</label>
```

##### Example 3

The following example shows a switch form element.

```html
<label class="form-control form-control--switch">
  <input name="newsletter" type="checkbox" />
  <span class="form-control-indicator"></span>
  Subscribe to newsletter
</label>
```

### Form range component

Form range is intended to create range form elements. 

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`form-range` | Applies a form range. | `<input class="form-range" type="range" />`
`form-range-label` | Applies a label above form range if needed. It can be useful to to show current value. | `<span class="form-range-label"></span>`

#### Examples

##### Example 1

The following example shows a range form element.

```html
<input id="price" class="form-range" type="range" min="0" max="100" step="1" />
```

### Form label component

Form label is intended to create labels for form elements. 

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`form-label` | Applies a form label. | `<label class="form-label"></label>`

#### Examples

##### Example 1

The following example shows a label and an input inside a form item.

```html
<div class="form-item">
  <label class="form-label" for="country">Country</label>
  <input name="country" id="country" class="form-input" type="text" />
</div>
```

### Form hint component

Form hint is intended to create hints under labels for form elements.

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`form-hint` | Applies a form hint. | `<span class="form-hint"></span>`

#### Examples

##### Example 1

The following example shows a label, hint and input inside a form item.

```html
<div class="form-item">
  <label class="form-label" for="country">Country</label>
  <span class="form-hint" id="countryTip">Please add a country name</span>
  <input name="country" id="country" class="form-input" type="text" aria-describedby="countryTip" />
</div>
```

### Form fieldset component

Form fieldset is intended to create fieldsets with a legend to group form elements.

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`form-fieldset` | Applies a form fieldset. | `<fieldset class="form-fieldset"></fieldset>`
`form-fieldset-legend` | Applies a form fieldset legend. | `<legend class="form-fieldset-legend"></legend>`
`form-fieldset-hint` | Applies a form fieldset hint. | `<span class="form-fieldset-hint"></span>`

#### Examples

##### Example 1

The following example shows an input with a label inside a fieldset with a legend and hint.

```html
<fieldset class="form-fieldset">
  <legend class="form-fieldset-legend">Shipping details</legend>
  <span class="form-fieldset-hint">Give your shipping address where you would like to receive orders.</span>
  <div class="form-item">
    <label class="form-label" for="country">Country</label>
    <input name="country" id="country" class="form-input" type="text" aria-describedby="countryTip" />
  </div>
</fieldset>
```

### Form group component

Form group is intended to group together input, select and textarea form elements.

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`form-group-list` | Applies a form group list. Use grid component for alignments. | `<ul class="form-group-list grid"></ul>`
`form-group-list-item` | Applies a form group list item. | `<li class="form-group-list-item grid-col"></li>`

#### Examples

##### Example 1

The following example shows two input form elements grouped together.

```html
<ul class="form-group-list grid grid--bottom">
  <li class="form-group-list-item grid-col grid-col--1of3">
    <div class="form-item">
      <label class="form-label" for="zip">ZIP</label>
      <input name="zip" id="zip" class="form-input" type="text" />
    </div>
  </li>
  <li class="form-group-list-item grid-col grid-col--fit">
    <div class="form-item">
      <label class="form-label" for="city">City</label>
      <input name="city" id="city" class="form-input" type="text" />
    </div>
  </li>
</ul>
```

### Form item component

Form item is intended to create wrappers for form elements.

#### Classes

Class name | Description | Example
---------- | ----------- | -------
`form-item` | Applies a form item. | `<div class="form-item"></div>`
`is-required` | Sets form item required. | `<div class="form-item is-required"></div>`

You can add additional information to a form item by adding `data-label` attribute to it. The value will be displayed under form element. It is useful to show validation errors combined with state colored form item extension idea.

#### Examples

##### Example 1

The following example shows a required input inside a form item.

```html
<div class="form-item is-required" data-label="Country is required">
  <label class="form-label" for="country">Country</label>
  <input name="country" id="country" class="form-input" type="text" aria-describedby="countryTip" />
</div>
```

#### Extension ideas

##### State colored form items

Add `generate-form-item` to each state in SCSS variables with the value of true or false. Then you can use form items in colors of enabled states. The extension can be useful for form validation.


```scss
/* Form item component extensions */
div.form-item {

  // State colored form items
  @each $state in map-keys($states) {
    @if (map-val($states, $state, generate-form-item)) {
      &.has-#{$state} {

        label.form-label, legend.form-label, span.form-hint, &:after {
          color: map-val($states, $state, bg-color);
        }
      }
    }
  }
}
```
