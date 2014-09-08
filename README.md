segmented-control
=================

A simple, CSS-driven way to create a segmented control using a list of radio buttons and labels.

Here’s the markup:
```html
<ul class="segmented-control">
    <li class="segmented-control__item"> <input class="segmented-control__input" type="radio" value="1"   name="option" id="option-1" checked>  <label class="segmented-control__label" for="option-1" > Thing 1</label> </li>
    <li class="segmented-control__item"> <input class="segmented-control__input" type="radio" value="2"   name="option" id="option-2" >         <label class="segmented-control__label" for="option-2" > Thing 2</label> </li>
</ul>
```


And the CSS:
```css
.segmented-control {
    display: table;
    width: 100%;
    margin: 2em 0;
    padding: 0;
}

.segmented-control__item {
    display: table-cell;
    margin: 0;
    padding: 0;
    list-style-type: none;
}

.segmented-control__input {
    position: absolute;
    visibility: hidden;
}

.segmented-control__label {
    display: block;
    margin: 0 -1px -1px 0; /* -1px margin removes double-thickness borders between items */
    padding: 1em .25em;

    border: 1px solid #ddd;

    font: 14px/1.5 sans-serif; 
    text-align: center;  

    cursor: pointer;
}

.segmented-control__label:hover {
    background: #fafafa;
}

.segmented-control__input:checked + .segmented-control__label {
    background: #eee;
    color: #333; 
}
```