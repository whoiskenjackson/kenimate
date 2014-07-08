##Animate CSS Example

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

##kenimate SCSS Example

```
.animated {
	
	@extend %animated;

}

.fadeIn {

	@extend %fadeIn;

}

@include flip-keyframes;
```

Or you could condense it down to:

```
.animated {
	
	@extend %animated;

}

.fadeIn {

	@extend %fadeIn;

}

@include flip-keyframes;
```