# Base SCSS

This is where all of the global SCSS helpers are stored.

1. Core

2. Variables

3. Fonts

4. Breakpoints

## Core

`_core.scss` loads in all of the necessary files located in the `/base` and `/widgets` directories. These are a library of helpers that can be (but are not required) to be used on various pages throughout the website.

## Variables

`_variables.scss` is a list of color and font variables that can easily be used throughout the site.

### Colors

  * `$black-01`: (#000). Pure black.
  * `$black-02`: (#0b0b0b). Footer, Menu button backgrounds, & (most) Page Titles.
  * `$white-01`: (#fff). Pure white.
  * `$gray-01`: (#333). Copy text color.
  * `$blue-01`: (#4dc0d3). Blue theme color.
  * `$orange-01`: (#c15316). Orange theme color.
  * `$yellow-01`: (#ebc701). Yellow theme color.

### Fonts

  * `$arial`: (Arial, "Helvetica Neue", Helvetica, sans-serif). Arial Web Font Family.
  * `$benchNine`: ('BenchNine', sans-serif). BenchNine Google Font Family.
  * `$noto`: ('Noto Serif', serif). Noto Google Font Family.
  * `$openSans`: ('Open Sans', sans-serif). Open Sans Google Font Family.

### Usage

The below example makes an `a` tag use the font family variable `$benchNine` and the color variable `$black-02`.

```
a {
  
    font-family: $benchNine;
    color: $black-02;
    font-size: 14px;

}
```

## Fonts

`_fonts.scss` is a list of font placeholders to be used across the site.

### Bench Nine

  * `%benchNine-400`: BenchNine with font weight 400.
  * `%benchNine-700`: BenchNine with font weight 700.

### Noto

  * `%noto-400`: Noto with font weight 400.
  * `%noto-700`: Noto with font weight 700.

### OpenSans

  * `%openSans-400`: Open Sans with font weight 400.
  * `%openSans-400-italic`: Open Sans with font weight 400 and font style italic.
  * `%openSans-700`: Open Sans with font weight 700.
  * `%openSans-700-italic`: Open Sans with font weight 700 and font style italic.
  * `%openSans-800`: Open Sans with font weight 800.

### Usage

The below example makes a `p` tag extend the `openSans-400` placeholder.

```
p {
    
    @extend %openSans-400;

    font-size: 14px;
    text-align: center;

}
```

## Breakpoints