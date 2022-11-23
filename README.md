# Number Spinner

[![npm version](https://badge.fury.io/js/number-spinner.svg)](https://badge.fury.io/js/number-spinner)
[![DragsterJS gzip size](http://img.badgesize.io/https://raw.githubusercontent.com/fluidweb-co/number-spinner/master/dist/number-spinner.min.js?compression=gzip
)](https://raw.githubusercontent.com/fluidweb-co/number-spinner/master/dist/number-spinner.min.js)

Add plus/minus buttons to input type number.



## Installation

Setting up is pretty straight-forward. Download the js files from __dist__ folder and include them in your HTML:

```html
<script type="text/javascript" src="path/to/dist/number-spinner.min.js"></script>
```

### NPM

Number Spinner is also available on NPM:

```sh
$ npm install number-spinner
```



## Initialization

Once the Number Spinner script is loaded all functions will be available through the global variable `window.NumberSpinner`, however to enable the components you need to call the function `init`:

Call the function `NumberSpinner.init( defaultOptions );` passing the `defaultOptions` parameter as an object.



## Options Available

The `options` parameter accept any of the available options from the default settings by passing the new values as an object. You can simply ommit the options you don't want to change the default values of.

These are the currently accepted options with their default values, if in doubt check the source code:

```js
	var _defaults = {
		bodyClass: 'has-number-spinner',

		containerSelector: '',
		inputSelector: 'input[type="number"]',

		buttonPlacement: 'both', // Accepts `both`, `before` and `after`.
		buttonsAddedClass: 'buttons-added',

		minusButtonTemplate: '<button type="button" class="number-spin-button minus" title="Decrease">-</button>',
		plusButtonTemplate: '<button type="button" class="number-spin-button plus" title="Increase">+</button>',

		onChangeCallback: null,
	};
```

For example, if your application already has the markup defined in many places and you want to change the selector used for the collapsible sections, initialize the component with the options below:

```js
var options = {
	containerSelector: 'body',
	buttonPlacement: 'after',
}
NumberSpinner.init( options );
```

Another use of the `options` object is to initialize multiple input fields on the page with differet options. In this case, you'll need to call the `init` function without the options parameter, and then call the function `initInputFields` function passing in the container element and the options for using on number input fields inside that container element:

```js
NumberSpinner.init();
NumberSpinner.initInputFields( document.querySelector( 'div.placement-before' ), { buttonPlacement: 'before' } );
NumberSpinner.initInputFields( document.querySelector( 'div.placement-after' ), { buttonPlacement: 'after' } );
```

Everything else will use the default values.


## Contributing to Development

This isn't a large project by any means, but you are definitely welcome to contribute.

### Development environment

Clone the repo and run [npm](http://npmjs.org/) install:

```
$ cd path/to/number-spinner
$ npm install
```

Run the build command:

```
$ gulp build
```

Build on file save:

```
$ gulp
$ gulp watch
```


## License

Licensed under MIT.
