#kenimate

SCSS Toolkit for quickly adding CSS Animations to projects. It's extending danedan's Animate CSS, and in the future will be adding other animations to the mix.

##Examples

Below are examples of both Animate CSS and kenimate. The goal was to make adding animations quick and painless.

###Animate CSS

```

.animated {

  -webkit-animation-duration: 1s;
  animation-duration: 1s;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;

}

.fadeIn {

  -webkit-animation-name: fadeIn;
  animation-name: fadeIn;

}

@-webkit-keyframes fadeIn {

  0% {

    opacity: 0;

  }

  100% {

    opacity: 1;

  }

}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}
```

###kenimate Example

```
.animated {
	
	@extend %animated;

}

.fadeIn {

	@extend %fadeIn;

}

@include fadeIn-keyframes;
```

Or you could condense it down to:

```
.fadeIn {

	@extend %animated;
	@extend %fadeIn;

}

@include fadeIn-keyframes;
```