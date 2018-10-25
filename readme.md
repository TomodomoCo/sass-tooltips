# sass-tooltips

**A portable Sass-based approach for simple text tooltips on arbitrary HTML elements.**

Install via `npm` (or `yarn` if that's your thing):

```
npm install --save-dev @tomodomo/sass-tooltips
```

## Usage

`sass-tooltips` is [eyeglass](https://github.com/sass-eyeglass/eyeglass)-aware. If you're using it, simply import with…

```scss
@import "sass-tooltips";
```

Otherwise, something like this should work:

```scss
@import "path/to/node_modules/@tomodomo/sass-tooltips/sass";
```

Then, in your HTML, add `data-tip-[direction]="Tooltip content here"` to the element you would like the tooltip targeted at, where `[direction]` is one of `tl`, `tm`, `tr`, `bl`, `bm`, or `br` (an abbreviation for top/bottom, left/middle/right). This corresponds to the direction the tooltip arrow is pointing.

For example:

```html
<a href="https://github.com/vanpattenmedia/vpm-tooltips" data-tip-tm="What an awesome tooltip library!">VPM Tooltips</a>
```

You can see how each direction is rendered in the screenshot below:

![Screenshot of the sass-tooltips library showing the directions that tooltips can point](https://raw.githubusercontent.com/TomodomoCo/sass-tooltips/gh-pages/screenshot.png)

## Options

The library can be customised with a number of variables. The variables, and their default values, are as follows:

```sass
$sass-tooltip--background: black;
$sass-tooltip--text-color: white;

$sass-tooltip--font-family: inherit;
$sass-tooltip--font-size: inherit;
$sass-tooltip--text-shadow: none;

$sass-tooltip--arrow-width: 0.875em;
$sass-tooltip--arrow-height: 0.6em;

$sass-tooltip--border-radius: 2px;
$sass-tooltip--padding: 0.45em 0.75em;
$sass-tooltip--z-index: 99;
```

## Caveats

The library makes use of `calc()`, and thus [will not work in IE8, Opera Mini, or earlier Android browsers](http://caniuse.com/calc). (A pull request that safely eliminates the `calc()` requirement would be [happily accepted](https://github.com/vanpattenmedia/vpm-tooltips/pulls)!)

Placing your tooltip text in the data attribute alone is _not sufficient for accessibility_. You might wish to set an `aria-label` attribute on your element, or use another recommended best practice to make sure you're accomomdating all users.

## Acknowledgements

This method of inserting tooltips was inspired by the [Daniel-Hug/tooltips](https://github.com/Daniel-Hug/tooltips) library.

## About Tomodomo

Tomodomo is a creative agency for magazine publishers. We use custom design and technology to speed up your editorial workflow, engage your readers, and build sustainable subscription revenue for your business.

Learn more at [tomodomo.co](https://tomodomo.co) or email us: [hello@tomodomo.co](mailto:hello@tomodomo.co)

## License & Conduct

This project is licensed under the terms of the MIT License, included in `LICENSE.md`.

All open source Tomodomo projects follow a strict code of conduct, included in `CODEOFCONDUCT.md`. We ask that all contributors adhere to the standards and guidelines in that document.

Thank you!
