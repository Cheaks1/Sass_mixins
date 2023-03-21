# Sass_mixins
this repository will contain all my sass mixins 

### Content of Mixins :
- [**Abselute**](#abselute-mixin)


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
