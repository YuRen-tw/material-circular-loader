# Material Circular Loader
Google Material design: [Progress & activity](https://www.google.com/design/spec/components/progress-activity.html)

## Usage
HTML
```html
<div class="circular">
  <div class="stroke-left"></div>
  <div class="stroke-right"></div>
</div> 
```
SCSS
```scss
.circular {
  @include loader_circle(stroke); // class name of stroke
}
```

## Size
Width and height are `2em`. (radius of circle is `1em`)  
Use `font-size` to change the loader size.

SCSS
```scss
.circular {
  @include loader_circle(stroke);
  font-size: 30px; // width and height become 60px
}
```

## Single Color
Use `color` to change the loader color.

SCSS
```scss
.circular {
  @include loader_circle(stroke);
  color: #2a74f6;
}
```

## Multiple Colors
HTML
```html
<div class="Cir my-color"> <!-- add a class -->
  <div class="S-left"></div>
  <div class="S-right"></div>
</div> 
```
SCSS
```scss
.Cir {
  @include loader_circle(S);
  @include loader_stroke_colors(
    L,
    my-color,
    (#4285f4, #ea4335, #fbbc05, #34a853)
  );
  // (classNameOfStroke, addedClassName, listOfColors)
}
```
There are some lists of colors can be used:

| List of colors       | Description           | Colors                   |
| -------------------- | --------------------- | ------------------------ |
| `$google_colors`     | Google main colors    | Blue, Red, Yellow, Green |
| `$google_colors_old` | (Old version)         |                          |
| `$g_plus_colors`     | Colors in Google+ app | 7 colors                 |