# Simple Button
[![Build status][travis-badge]][travis-url] [![Bower dependencies][bowerdeps-badge]][bowerdeps-url] ![Version][bower-badge] ![Size][size-badge] [![Published][webcomponents-badge]][webcomponents-url]

Simple button extends the navtive `<button>` element to make it better behaved. It strips all vendor styles, adds an `icon` property, and a `busy` state that toggles a spinner and fires events. 

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="../iron-icons/iron-icons.html">
    <link rel="import" href="simple-button.html">
    <style>
      button[is="simple-button"] {
        font-family: sans-serif;
        font-size: 14px;
        color: white;
        float: left;
        border-radius: 5px;
        padding: 0.5em 1em;
        margin: 15px 15px 0 0;
        background: rgb(76, 208, 204);
      }
    </style>
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<!-- Buttons with basic styles applied -->
<button is="simple-button" id="busy">do something</button>
<button is="simple-button" icon="icons:thumb-up">like</button>

<script>
  var busyButton = document.querySelector('#busy');
  busyButton.addEventListener('click', function() {
    busyButton.busy = true;
  });
</script>
</script>
```

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

Properties can either be set as attributes on the element, or imperitively with Javascript

```html
<button is="simple-button" icon="" align="left"></button> 

<script>
  document.querySelector('button[is="simple-button"]').busy = true;
</script>
```

## Styling
In addition to applying styles to the button itself, you can style specific parts of simple-button with custom CSS properties

Property                      | Default   | Description                                                          
----------------------------- | --------- | ------------                                                         
`--simple-button-icon-size`   | `1em`     | Size of the button icon, defaults to 1em so you can use `font-size`. 
`--simple-button-icon-offset` | `0.35em`  | Margin between icon and button text content.                         

--

MIT © [Simpla](https://www.simpla.io)

[webcomponents]: https://github.com/webcomponents/webcomponentsjs
[iron-icons]: https://elements.polymer-project.org/elements/iron-icons?view=demo:demo/index.html
[iron-iconset]: https://elements.polymer-project.org/elements/iron-iconset-svg

[bower-badge]: https://img.shields.io/bower/v/simple-button.svg
[bowerlicense-badge]: https://img.shields.io/bower/l/simple-button.svg
[travis-badge]: https://img.shields.io/travis/SimpleElements/simple-button.svg
[travis-url]: https://travis-ci.org/SimpleElements/simple-button
[bowerdeps-badge]: https://img.shields.io/gemnasium/SimpleElements/simple-button.svg
[bowerdeps-url]: https://gemnasium.com/bower/simple-button
[size-badge]: https://badges.herokuapp.com/size/github/SimpleElements/simple-button/master/simple-button.html?gzip=true&color=blue
[webcomponents-badge]: https://img.shields.io/badge/webcomponents.org-published-blue.svg
[webcomponents-url]: https://www.webcomponents.org/element/SimpleElements/simple-button