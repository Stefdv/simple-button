# Simple Button
[![Build status][travis-badge]][travis-url] [![Bower dependencies][bowerdeps-badge]][bowerdeps-url] ![Version][bower-badge] ![Size][size-badge]
<br/>[![Cross browser test status][browser-badges]][travis-url]

Extends the `<button>` element with extra functionality and fewer styles. 

Strips all default `button` styles, adds an `icon` property that lets you insert SVG icons in the button, and a `busy` state that toggles a spinner and fires events.

## Installation & usage

Install simple-button with Bower

```sh
$ bower install simple-button --save
```

Import it into the `<head>` of your page

```html
<link rel="import" href="/bower_components/simple-button/simple-button.html">
```

Then use it in your project, by extending the native `<button>` element.

```html
<button is="simple-button"></button>
```

Note for cross-browser support you should also include the [Web Components Polyfill][webcomponents].

## Options
Simple Button adds several extra properties and behaviors to the standard `button` element.

Property      | Type    | Default           | Description                                                                                                                
------------- | ------- | ----------------- | ------------                                                                                                                 
`icon`        | String  | `''`              | SVG definition of an icon. Use [`iron-icons`][iron-icons], or define your own iconset with [`iron-iconset`][iron-iconset]. 
`busy`        | Boolean | `false`           | Set the busy state of the button. Shows a busy spinner when true.                                                          
`align`       | String  | `'left'`          | Set the alignment of button icon, busy spinner, and text. Can be `'left'` or `'right'`.                                         

```html
<button is="simple-button" icon="" align="left"></button> 
```

## Styling
In addition to applying styles to the button itself, you can style specific parts of simple-button with custom CSS properties

Property                      | Default   | Description                                                          
----------------------------- | --------- | ------------                                                         
`--simple-button-icon-size`   | `1em`     | Size of the button icon, defaults to 1em so you can use `font-size`. 
`--simple-button-icon-offset` | `0.35em`  | Margin between icon and button text content.                         

--

MIT © 2016 [Simpla](https://www.simpla.io)

[webcomponents]: https://github.com/webcomponents/webcomponentsjs
[iron-icons]: https://elements.polymer-project.org/elements/iron-icons?view=demo:demo/index.html
[iron-iconset]: https://elements.polymer-project.org/elements/iron-iconset-svg
[spinkit]: http://tobiasahlin.com/spinkit/

[bower-badge]: https://img.shields.io/bower/v/simple-button.svg
[bowerlicense-badge]: https://img.shields.io/bower/l/simple-button.svg
[travis-badge]: https://img.shields.io/travis/SimpleElements/simple-button.svg
[travis-url]: https://travis-ci.org/SimpleElements/simple-button
[bowerdeps-badge]: https://img.shields.io/gemnasium/SimpleElements/simple-button.svg
[bowerdeps-url]: https://gemnasium.com/bower/simple-button
[size-badge]: https://badges.herokuapp.com/size/github/SimpleElements/simple-button/master/simple-button.html?gzip=true&color=blue
[browser-badges]: https://badges.herokuapp.com/travis/SimpleElements/simple-button/sauce/SimpleElements?labels=none
