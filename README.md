# Archetype

A minimal stylesheet for beautiful typography.

## Usage

Add `archetype.css` to your HTML:

```html
<!-- Add Archetype -->
<link rel="stylesheet" type="text/css" href="archetype.css">

<!-- Your style sheet -->
<link rel="stylesheet" type="text/css" href="main.css">
```

then make sure your style sheet (`main.css` in the example above) has the
following set:

```css
html {
  /* Pick the font size you want. Archetype will adapt. */
  font-size: 16px;
}

body {
  /* Choose your preferred font. */
  font-family: "Source Sans Pro", sans-serif;
}
```

And you're done!

If you want to change anything in Archetype, just override it in your
`main.css` sheet.


## Correcting for fonts' actual pixel sizes

If you are using a font that is always visually smaller than other fonts at the
same `font-size` setting, Archetype can look too "spread out" or too "tight". To
adjust for that, set the following property in CSS before loading
`archetype.css`:

```css
:root {
  --archetype-correction: 1.0;
}
```

If you set it to a value greater than `1`, such as `1.1`, more space will be
added everywhere. If smaller than `1`, everything will be laid out tighter.
