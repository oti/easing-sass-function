
# Easing Sass Function

https://easing-sass-function.dskd.jp

Inspired by [easing.net](https://easing.net).

[![Netlify Status](https://api.netlify.com/api/v1/badges/01ab9f61-7c5a-4d85-a34e-2f9c4cae11bb/deploy-status)](https://app.netlify.com/sites/easing-sass-function/deploys)

- **v2.x is compatible to dart-sass**
- [v1.x](https://github.com/oti/easing-sass-function/releases/tag/v1.2.0) is compatible to libsass(node-sass).

## You can get custom easing sass function

```sass
@use "sass:map";

$easing-map: (
  easeInSine:     cubic-bezier(0.47, 0, 0.745, 0.715),
  easeOutSine:    cubic-bezier(0.39, 0.575, 0.565, 1),
  easeInOutSine:  cubic-bezier(0.445, 0.05, 0.55, 0.95),

  easeInQuad:     cubic-bezier(0.55, 0.085, 0.68, 0.53),
  easeOutQuad:    cubic-bezier(0.25, 0.46, 0.45, 0.94),
  easeInOutQuad:  cubic-bezier(0.455, 0.03, 0.515, 0.955),

  easeInCubic:    cubic-bezier(0.55, 0.055, 0.675, 0.19),
  easeOutCubic:   cubic-bezier(0.215, 0.61, 0.355, 1),
  easeInOutCubic: cubic-bezier(0.645, 0.045, 0.355, 1),

  easeInQuart:    cubic-bezier(0.895, 0.03, 0.685, 0.22),
  easeOutQuart:   cubic-bezier(0.165, 0.84, 0.44, 1),
  easeInOutQuart: cubic-bezier(0.77, 0, 0.175, 1),

  easeInQuint:    cubic-bezier(0.755, 0.05, 0.855, 0.06),
  easeOutQuint:   cubic-bezier(0.23, 1, 0.32, 1),
  easeInOutQuint: cubic-bezier(0.86, 0, 0.07, 1),

  easeInExpo:     cubic-bezier(0.95, 0.05, 0.795, 0.035),
  easeOutExpo:    cubic-bezier(0.19, 1, 0.22, 1),
  easeInOutExpo:  cubic-bezier(1, 0, 0, 1),

  easeInCirc:     cubic-bezier(0.6, 0.04, 0.98, 0.335),
  easeOutCirc:    cubic-bezier(0.075, 0.82, 0.165, 1),
  easeInOutCirc:  cubic-bezier(0.785, 0.135, 0.15, 0.86),

  easeInBack:     cubic-bezier(0.6, -0.28, 0.735, 0.045),
  easeOutBack:    cubic-bezier(0.175, 0.885, 0.32, 1.275),
  easeInOutBack:  cubic-bezier(0.68, -0.55, 0.265, 1.55)
);

@function easing($name) {
  @return map.get($easing-map, $name);
}
```

## Usage

### from git

1. git clone and move to your project.

```shell
git clone git@github.com:oti/easing-sass-function.git
mv easing-sass-function/src/_easing-sass-function.scss your/project/scss/path
```

2. @use in your .scss file.

```sass
@use 'your/project/scss/path/easing-sass-function' as *;
```

### from npm

1. npm insatall.

```shell
npm i easing-sass-function
```

2. `@use` in your .scss file.

```sass
@use '../(to project root)/node_modules/easing-sass-function';
```

1. write `easing()` sass function.

```sass
.elem {
  transition-timing-function: easing(easeInSine);
}
```

## LICENSE

[MIT license Copyright (c) 2018 oti](LICENSE.txt)
