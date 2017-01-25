# blueq

**blueq** is a collection of Sass mixins and functions for generating media queries and managing breakpoints

It is developed and maintained internally at [bluegrassdigital](http://www.bluegrassdigital.com), but feel free to contribute!

## Installation

`npm install blueq`

## Example usage

```scss
@import 'blueq/main.scss';

$blueq-breakpoints: (
  s: 320px,
  m: 576px,
  l: 768px,
  xl: 1024px,
  xxl: 1200px
);

// Min width media query
.foo {
  @include blueq-min('l') {
    width: 50%;
    float: left;
  }
}

// Max width media query
.foo {
  width: 50%;
  float: left;
  @include blueq-max('l') {
    width: auto;
    float: none;
  }
}
// Output
// Max width queries are adjusted by 1px, pass false as the second mixin argument to disable
@media (max-width: 767px) { 
  .foo {
    width: 50%;
    float: left;
  }
}

// Min and max width media queries
.foo {
  @include blueq-minmax('l', 'xxl') {
    width: 50%;
    float: left;
  }
}

```
## API

See <a href="http://bluegrassdigital.github.io/blueq/index.html" target="_blank">API docs</a>

## Contributing to nestable-grid

[Github Flow](https://guides.github.com/introduction/flow/) - branch, submit pull requests
