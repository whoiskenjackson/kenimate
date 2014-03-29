# Widgets SCSS

This is where all of the global SCSS helpers are stored.

  1. [Image Replace](#image-replace)

  2. [Inline Block](#inline-block)

  3. [Sprites](#sprites)

  4. [Clear Fix](#clear-fix)

## Image Replace

This is located in `_image-replace.scss`. This is a placeholder for an implementation of replacing text with a background image. It is based off of Twitter Bootstrap's implementation. This is utilized to maintain SEO value of tags like: h1, h2, h3.

```
%image-replace {

	font: 0/0 a;
	color: transparent;
	text-shadow: none;
	border: 0;
	background-repeat: no-repeat;
	background-position: center center;

}
```

### Usage

The example below will make the `h1` tag be replaced with a background image by hiding the text.

```
h1 {

	@extend %image-replace;

	width: 200px;
	height: 20px;
	display: block;
	background-image: url('images/someTitle.png');

}
```

## Inline Block

This is located in `_inline-block.scss`. This is a placeholder for a cross browser implementation of inline block. It utilizes a Compass Mixin to do the bulk of the work.

```
%inline-block {

	@include inline-block;
	vertical-align: top;

}
```

### Usage

The example below will make all `li` tags `display: inline-block`.

```
li {
	
	@extend %inline-block;

	list-style: none;

}
```

## Sprites

This is located in `_sprites.scss`. This is a mixin that is used to quickly go through a sprite image and setup an element with a sprite. You can use this mixin in other SCSS files, or you can create a placeholder in this file to use in other SCSS files.

```
@mixin sprite($width, $height, $left: 0, $top: 0, $leftHover: 0, $topHover: 0) {
	
	width: $width;
	height: $height;
	background: url(/wp-content/themes/fit/images/sprites.png) $left $top no-repeat;
	
	&:hover{
	
		background-position: $leftHover $topHover;
	
	}

}
```

### Requirements

  * For the Mixin, you can pass in up to six values: `width, height, left position, top position, hover left position, hover top position`.
  * The only required values are `width, height`.
  * If there is no hover state available, then you'll need to use the `left position, top position` values for the `hover left position, hover top position` values.


### Usage

The example below will create a placeholder for a facebook sprite. This placeholder would be placed in `_sprites.scss`.

```
%sprite-social-fb {

	@include sprite(21px, 20px, -28px, -110px, -28px, -110px);

}
```

You could then use this placeholder anywhere on the site.

```
.fb {
	
	@extend %sprite-social-fb;

	display: block;

}
```

## Clear Fix

This is located in `_clear-fix.scss`. This is a placeholder used on an element that will clear the floating elements inside.

```
%clear-fix {
	
	&:before,
	&:after {

		content: " ";
		display: table;
	
	}

	&:after {
	
		clear: both;
	
	}

}
```

### Usage

The below example has floating `a` tags inside of a `nav` element. To make sure the `nav` element clears, we use the `%clear-fix` placeholder.

```
nav {
	
	@extend %clear-fix;

	a {

		display: block;
		float: left;
		width: 20px;
		height: 20px;

	}

}
```

## Animations