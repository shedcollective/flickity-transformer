# Flickity Transformer
*Transform your Flickity*

Flickity Transformer enhances [Flickity](http://flickity.metafizzy.co/) with exciting effects through the use of CSS transform functions.

- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)

## Installation
Via NPM:

```bash
npm i --save flickity-transformer
```

## Usage
```js
var Flickity = require('flickity')
var FlickityTransformer = require('flickity-transformer')

var flckty = new Flickity('.carousel', {
  // options
})

// Create a new instance of FlickityTransformer, passing in your `flckty` instance and a configuration object that contains an array of `transforms`. Each transform should have a `name` property, corresponding to the transform function you want to use, and a `stops` array, containing at least two stops. Each stop is an array with two values: x position in pixels relative to the home position of your carousel, and the transform value to apply at that position.
var ftx = new FlickityTransformer(flckty, {
  transforms: [
    {
      name: 'scale',
      stops: [
        [-300, 0.5],
        [0, 1],
        [300, 0.5]
      ]
    },
    {
      name: 'rotate',
      stops: [
        [-300, -45],
        [0, 0],
        [300, 45]
      ]
    }
  ]
})
```

## Examples
Coming soon...

## Contributing
Contributions are welcome.

### TODO

- Add support for more transform functions.
- Add ability to use units other than the defaults.
- Replace d3-scale dependency with a lighter-weight linear scale that supports clamping and piecewise scales.
- More useful tests.
- Test against all Flickity features (e.g. wrapAround is not currently supported).
