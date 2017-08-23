# Simple Button
[![Build status][travis-badge]][travis-url] ![Size][size-badge] [![Version][tag-badge]][releases-url] [![Published][webcomponents-badge]][webcomponents-url]

A lightweight, high quality, style-agnostic, form-friendly button component, built on Web Components. `<simple-button>` is a drop-in upgrade for HTML's `<button>` element. 

<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
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
<!-- Extremely lightweight -->
<simple-button>naked button</simple-button> 

<!-- Easy to style -->
<simple-button class="fancy">fancy button</simple-button>

<!-- Comes with superpowers -->
<simple-button class="fancy" busy>working...</simple-button>

<style>
  .fancy {
    font-size: 14px;
    color: white;
    border-radius: 5px;
    padding: 0.5em 1em;
    background: rgb(76, 208, 204);
  }
</style>
```

### Contents

- [Features](#features)
- [Installation & usage](#installation--usage)
  - [Polyfills for cross-browser support](#polyfills-for-cross-browser-support)
  - [Transpiling for IE11 support](#transpiling-for-ie11-support)
- [Options](#options)
- [Styling](#styling)

## Features

- No default UI, style it however you like
- Works seamlessly as a submit button for forms
- `busy` state that opens in-button spinner and disables user interaction
- `icon` property that displays an SVG icon definition

## Installation & usage

Install simple-button with Bower

```sh
$ bower i SimpleElements/simple-button --save
```

Import it into the `<head>` of your page

```html
<link rel="import" href="/bower_components/simple-button/simple-button.html">
```

Then use simple-button in your project

```html
<simple-button>click me!</simple-button>
```

### Polyfills for cross-browser support

simple-button relies on emerging standards, for full cross-browser support include the [WebComponentsJS](https://github.com/webcomponents/webcomponentsjs) polyfill on your page.

```html
<script src="https://unpkg.com/@webcomponents/webcomponentsjs@^1.0.0/webcomponents-loader.js"></script>
```

### Transpiling for IE11 support

Web Components like simple-button are distributed as ES6 classes, which are supported in all evergreen browsers. To support Internet Explorer 11 you should transpile simple-button to ES5 and use the `webcomponentsjs` `custom-elements-es5-adapter.js` shim. 

The easiest way to do this is by including [polymer-build][polymer-build] in your buildstep of choice. Then just include the ES5 adapter on your page

```html
<script src="https://unpkg.com/@webcomponents/webcomponentsjs@^1.0.0/custom-elements-es5-adapter.js"></script>
```

## Options

Simple-button adds several extra properties and behaviors compared to the standard `<button>` element.

Property      | Type    | Default           | Description                                                                                                                
------------- | ------- | ----------------- | ------------                                                                                                                 
`icon`        | String  | `''`              | SVG definition of an icon. Use [`iron-icons`][iron-icons], or define your own iconset with [`iron-iconset-svg`][iron-iconset-svg]. 
`busy`        | Boolean | `false`           | Set the busy state of the button. Shows a busy spinner when true.                                                          
`align`       | String  | `'left'`          | Set the alignment of button icon and busy spinner. `'left'` or `'right'`.                                         

Properties can either be set as attributes on the element, or imperitively with Javascript

```html
<simple-button align="left"></simple-button> 

<script>
  document.querySelector('simple-button').busy = true;
</script>
```

## Styling
In addition to styling the button itself, you can style specific parts of simple-button with custom CSS properties

Property                      | Default   | Description                                                          
----------------------------- | --------- | ------------                                                         
`--simple-button-icon-size`   | `1em`     | Size of the button icon, defaults to 1em so you can use `font-size`

Apply custom CSS props directly on simple-button

```css
simple-button {
  --simple-button-icon-size: 14px;
}
```

***

MIT © [Sean King](https://twitter.com/seaneking)

[tag-badge]: https://img.shields.io/github/tag/SimpleElements/simple-button.svg
[releases-url]: https://github.com/SimpleElements/simple-button/releases
[travis-badge]: https://img.shields.io/travis/SimpleElements/simple-button.svg
[travis-url]: https://travis-ci.org/SimpleElements/simple-button
[size-badge]: http://img.badgesize.io/SimpleElements/simple-button/master/simple-button.html?compression=gzip&label=size%20%28unminified%29
[webcomponents-badge]: https://img.shields.io/badge/webcomponents.org-published-blue.svg
[webcomponents-url]: https://www.webcomponents.org/element/SimpleElements/simple-button
