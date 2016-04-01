# Material Circular Loader
Google Material design: [Progress & activity](https://www.google.com/design/spec/components/progress-activity.html)

## Usage
HTML
```html
<div class="circular">
  <div class="line-left"></div>
  <div class="line-right"></div>
</div> 
```
SCSS
```scss
.circular {
  @include loading_circle(line); // class name of line
}
```

## Size
Width and height are `2em`. (radius of circle is `1em`)  
Use `font-size` to change the loader size.

SCSS
```scss
.circular {
  @include loading_circle(line);
  font-size: 30px; // width and height become 60px
}
```

## Single Color
Use `color` to change the loader color.

SCSS
```scss
.circular {
  @include loading_circle(line);
  color: #2a74f6;
}
```

## Multiple Colors
HTML
```html
<div class="Cir my-color"> <!-- add a class -->
  <div class="L-left"></div>
  <div class="L-right"></div>
</div> 
```
SCSS
```scss
.Cir {
  @include loading_circle(L);
  @include loading_line_color(
    L,
    my-color,
    (#4285f4, #ea4335, #fbbc05, #34a853)
  );
  // (classNameOfLine, addedClassName, ListOfColors)
}
```
There are some lists of colors can be used:

| List of colors      | Description           | Colors                   |
| ------------------- | --------------------- | ------------------------ |
| `$google_color`     | Google main colors    | Blue, Red, Yellow, Green |
| `$google_color_old` | (Old version)         |                          |
| `$g_plus_color`     | Colors in Google+ app | 7 colors                 |