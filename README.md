# Chardin.js

**Simple overlay instructions for your apps.**

[Check out a demo](http://yudao.github.com/chardin.js/).

Chardin.js is a jQuery plugin that creates a simple overlay to display instructions on existent elements. It is inspired by
the recent Gmail new composer tour which I loved.

You can display instructions in a sequenced manner with automatic delay or by a simple click.

![chardin](https://raw.github.com/heelhook/chardin.js/master/example/img/chardin.png "chardin")  
[Jean-Baptiste-Siméon Chardin](http://en.wikipedia.org/wiki/Jean-Baptiste-Sim%C3%A9on_Chardin)

## Installing

Simple! Fork this repo or download [chardinjs.css][0] and [chardinjs.min.js][1] and add the following assets to your HTML:

```HTML
<link href="chardinjs.css" rel="stylesheet">
<script src="chardinjs.min.js"></script>
```

### Installing in the rails asset pipeline (optional) 

There's a [`chardinjs-rails`](https://github.com/heelhook/chardin.js-rails) gem.

### Building (optional)

If you choose to fork the repo you can build the assets running

    rake compile


## Adding data for the instructions

Add the instructions to your container for sequenced mode:

`data-sequenced`: True to run the sequenced mode
`data-auto`: True if you want to pass to each instructions automatically
`data-delay`: Number of milliseconds for the delay of the auto mode

Add the instructions to your elements:

`data-intro`: Text to show with the instructions  
`data-position`: (`left`, `top`, `right`, `bottom`), where to place the text with respect to the element
`data-sequence`: Number to sort ascending the instruction (only for sequenced mode)

```HTML
<img src="img/chardin.png" data-intro="An awesome 18th-century painter, who found beauty in everyday, common things." data-position="right" />
```

## Running

Once you have your elements ready you can show instructions running

```Javascript
$('body').chardinJs('start')
```

If you would rather run ChardinJs confined to a particular container (instead of using the whole document) you can
change `body` to some other selector.

```Javascript
$('.container').chardinJs('start')
```

In sequence mode, you can click to the right of the screen to pass to the next instruction and to the left of the screen to pass to the previous instruction.


## Methods

### .chardinJs('start')

Start ChardinJs in the selector.

### .chardinJs('toggle')

Toggle ChardinJs.

### .chardinJs('stop')

Make your best guess. That's right! Stops ChardinJs in the selector.

### .chardinJs('next')

Go to the next instruction (only in sequenced mode)

### .chardinJs('previous')

Return to the previous instruction (only in sequenced mode)

## Events

### 'chardinJs:start'

Triggered when chardinJs is correctly started.

### 'chardinJs:stop'

Triggered when chardinJs is stopped.

### 'chardinJs:next'

Triggered when chardinJs pass to the next helper. (Only in sequenced mode).

### 'chardinJs:previous'

Triggered when chardinJs pass to the previous helper. (Only in sequenced mode).

## Author

[Pablo Fernandez][2]

### Contributors

 * [John Weir](https://github.com/jweir)
 * [felipeclopes](https://github.com/felipeclopes)
 * [Bobby Jack](https://github.com/fiveminuteargument)
 * [Maxim Syabro](https://github.com/syabro)
 * [nmeum](https://github.com/nmeum)
 * [printercu](https://github.com/printercu)
 * [Mickaël Gentil](https://github.com/yudao)

## Contributions

If you want to contribute, please:

  * Fork the project.
  * Make your feature addition or bug fix.
  * Add yourself to the list of contributors in the README.md.
  * Send me a pull request on Github.

## License

Copyright 2013 Pablo Fernandez

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

 [0]: https://github.com/heelhook/chardin.js/blob/master/chardinjs.css
 [1]: https://github.com/heelhook/chardin.js/blob/master/chardinjs.min.js
 [2]: https://github.com/heelhook


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/heelhook/chardin.js/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

