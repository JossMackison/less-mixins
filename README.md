LESS Mixins
===========

A collection of mixins I use in most projects.

####.fill-space(top, right, bottom, left)

Fill all available space provided by an element's parent.

Note: Apply "auto" appropriately if the element has a fixed width/height.

```less
.site {
	.fill-space();
}
.site-header() {
	.fill-space(0, 0, auto, 0);
	height: @header-height;
}
.site-body() {
	.fill-space(@header-height, 0, 0, 0);
}
```

####.scrollable(direction)

Areas will sometimes lose their ability to scroll when manipulated, particularly iOS. This mixin will re-introduce correct scrolling behaviour

```less
.fake-body {
	.scrollable(y);
}
```

####.inline-align(alignment)

A simpler way to set display inline when you also want to align the lateral axis. Defaults to "middle".

```less
.list li {
	.inline-align(bottom);
}
```