LESS Mixins
===========

A collection of mixins I use in most projects.



### .flexbox() | .flex(values) | .flexorder(val)

Start using flexbox today without worrying about vendor prefixes.

```less
.wrapper {
	&:extend(.flexbox all);
}
.item {
	.flex(1 200px);
	.flexorder(2);
}
```




### .fonticon(color, content, size)

Use with your favourite icon font family. Apply to pseudo elements (:before, :after)

```less
.icon {
	...
	
	&:after {
		.fonticon(#ff0000, '\2665', 2em);
	}
}
```




### Map Crop (utility)

For responsive Google map images - changing the proportions of static Google
map with "max-width: 100%" results in illegible place names.

The container ".mapcrop" behaves like a mask so the image is free to extend
left and right inside it.

```html
<div class="mapcrop mapcrop--md">
	<img class="mapcrop__map" width=640 height=160 src="..." alt="...">
</div>
```




### .fill-space(top, right, bottom, left)

Fill all available space provided by an element's parent.

###### Use "auto" to control elements that have fixed width/height.

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



### .scrollable(direction)

Areas will sometimes lose their ability to scroll when manipulated, particularly iOS. This mixin will re-introduce correct scrolling behaviour

```less
.wrapper {
	.scrollable(y);
}
```



### .inline-align(alignment)

A simpler way to set display inline when you also want to align the lateral axis. Defaults to "middle".

```less
.list > li {
	.inline-align(bottom);
}
```
