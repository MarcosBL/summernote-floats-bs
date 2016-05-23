## Bootstrap Floats for [Summernote WYSIWYG Editor](http://summernote.org/)

Replace (or extend) image popover buttons (using float: attributes) with a new set of buttons that inject proper Bootstrap classes (pull-right / pull-left / none) while keeping any other class in the image.

This not only keeps Bootstrap naming convention, but makes it much easier to style margins/paddings/etc on floated images, as you can just target the classes.

You can try a demo at http://marcosbl.github.io/summernote-floats-bs/demo/

![Screenshot](screenshot.jpg?raw=true "Screenshot")

## Installation

First include ````summernote-floats-bs.js```` or it's minified version ````summernote-floats-bs.min.js```` after ````summernote````

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/summernote/0.8.1/summernote.min.js"></script>

<script src="summernote-floats-bs.min.js"></script>
```

## Usage

Then just initialize the toolbar replacing the float buttons ```( floatBSLeft / floatBSRight / floatBSNone )```

```js
$(document).ready(function() {
	$('#texto').summernote({
		lang: 'en-US',
		dialogsInBody: true,
		popover: {
			image: [
			['imagesize', ['imageSize100', 'imageSize50', 'imageSize25']],
			/* ['float', ['floatLeft', 'floatRight', 'floatNone']], */
			/* Those are the old regular float buttons */
			['floatBS', ['floatBSLeft', 'floatBSNone', 'floatBSRight']],
			/* Those come from the BS plugin, in any order, you can even keep both! */
			['remove', ['removeMedia']],
			],
		}
	});
});
```