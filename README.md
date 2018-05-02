
# Easing Sass Function

For using [easings.net](http://easings.net/) with Sass function.

## Overview

cubic-bezier collection with data-map and sass-function.

```Sass
// _easing-var.scss
$ease-map: (
  easeInSine:     cubic-bezier(0.47, 0, 0.745, 0.715),
  easeOutSine:    cubic-bezier(0.39, 0.575, 0.565, 1),
  easeInOutSine:  cubic-bezier(0.445, 0.05, 0.55, 0.95),
  ...
  ...
);
```

```Sass
// _easing-var.scss
@function ease($name) {
  @return map-get($ease-map, $name);
}
```

## Visual Sample

https://oti.github.io/easing-sass-function/test/

## Usage

### from git

1. git clone and move to your project.

```shell
git clone git@github.com:oti/easing-sass-function.git
mv easing-sass-function/src/_easing-var.scss <your project>/<scss dirctory>
mv easing-sass-function/src/_easing-function.scss <your project>/<scss dirctory>
```

2. `@import` in your .scss file.

```Sass
// Example
@import '<your scss partial file directory>/easing-var';
@import '<your scss partial file directory>/easing-function';
```

3. write `ease()` sass function and argument in value of transition-timing-function.

```Sass
// Example
.line {
  transiton-property: transform;
  transiton-duration: 0.125s
  transiton-timing-function: ease(easeInOutBack)
}
```

### from npm

1. npm insatall.

```shell
npm i easing-sass-function
```

2. `@import` in your .scss file.

```Sass
// Example
@import '../(to project root)/node_modules/easing-sass-function/src/easing-var';
@import '../(to project root)/node_modules/easing-sass-function/src/easing-function';
```

3. write `ease()` sass function and argument in value of transition-timing-function.

```Sass
// Example
.line {
  transiton-property: transform;
  transiton-duration: 0.125s
  transiton-timing-function: ease(easeInOutBack)
}
```

## LICENSE

[MIT license Copyright (c) 2018 oti](LICENSE.txt)
