
# Easing Sass Function

For using [easings.net](http://easings.net/) with Sass function.

## Overview

cubic-bezier collection by data-map and sass-function.

```Sass
$ease-map: (
  easeInSine:     cubic-bezier(0.47, 0, 0.745, 0.715),
  easeOutSine:    cubic-bezier(0.39, 0.575, 0.565, 1),
  easeInOutSine:  cubic-bezier(0.445, 0.05, 0.55, 0.95),
  ...
  ...
);


@function ease($name) {
  @return map-get($ease-map, $name);
}
```

## Usage

1. git clone and move to your project.

```shell
git clone git@github.com:oti/easing-sass-function.git
mv easing-sass-function/src/_easing-sass-function.scss <your project>/<scss dirctory>
```

2. `@import` in your .scss file.

```Sass
// Example
@import '<your scss partial file directory>/easing-sass-function';
```

3. write `ease()` sass function and argument in value of transition-timing-function.

```Sass
// Example
.line {
  transiton-property: transform;
  transiton-duration: 0.125s
  transiton-timing-function: <mark>ease(easeInOutBack)</mark>
}
```

Argument of `ease()` is easing name. there are key of `$ease-map()`.

## LICENSE

[MIT.](LICENSE.md)
