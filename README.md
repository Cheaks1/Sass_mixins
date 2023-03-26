# Sass_mixins
this repository will contain all my sass mixins 

### Content of Mixins :
- [**Abselute**](#abselute-mixin)
- [**Centering**](#centering-mixin)


## Abselute Mixin:
This mixin sets the position property of an element to absolute 
and sets the values of the **top, bottom, right, and left** properties based on the values passed as parameters.
```
@mixin abselute ($top :null, $bottom:null, $right:null, $left :null) {
    position: absolute;
    top: $top;
    left: $left;
    bottom: $bottom;
    right: $right;
}
```
If any of the four parameters are provided with a **non-null value**, their corresponding CSS properties are set to that value. If a parameter is not provided or is passed a **null value**, the corresponding CSS property is **not set**.

**Here's an example of how you might use the "abselute" mixin in your SCSS code:**
```
.my-element {
  @include abselute($top: 20px, $left: 10px);
}

```
**This generates the following CSS code:**

```
.my-element {
  position: absolute;
  top: 20px;
  left: 10px;
}

```

**Note:** that the **"bottom"** and **"right"** properties are not set in this example, because they were not provided as arguments to the mixin.




## Centering Mixin:

This code is an example of a **CSS mixin** that can be used to center an element **horizontally and vertically** within its parent container.

```
@mixin centering {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

- ``position: absolute``: This positions the element relative to its nearest positioned ancestor, which is typically the parent container.
- ``top: 50% and left: 50%``: These set the element's position to be in the center of its parent container, but only horizontally and vertically aligned by 50%.
- ``transform: translate(-50%, -50%)``: This adjusts the position of the element by moving it 50% of its width to the left and 50% of its height up, effectively centering it completely.
