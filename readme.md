# VPM Tooltips

**A portable Sass-based approach for simple text tooltips on arbitrary HTML elements.**

This library is intended to be installed via Bower, but you can also download the `sass/_tooltips.scss` file directly into your project.

## Usage

After `@import`-ing the file, add `data-tip-[direction]="Tooltip content here"` to the element you would like the tooltip targeted at, where `[direction]` is one of `tl`, `tm`, `tr`, `bl`, `bm`, or `br` (an abbreviation for top/bottom, left/middle/right). This corresponds to the direction the tooltip arrow is pointing.

For example:

```html
<a href="https://github.com/vanpattenmedia/vpm-tooltips" data-tip-tm="What an awesome tooltip library!">VPM Tooltips</a>
```

You can see how each direction is rendered in the screenshot below:

![Screenshot of VPM Tooltips in action](https://raw.githubusercontent.com/vanpattenmedia/vpm-tooltips/gh-pages/screenshot.png)

## Options

There are a number of Sass variables you can customise. The variables, and their default values, are as follows:

```sass
$vpm-tooltip--background: black;
$vpm-tooltip--text-color: white;

$vpm-tooltip--font-family: inherit;
$vpm-tooltip--font-size: inherit;
$vpm-tooltip--text-shadow: none;

$vpm-tooltip--arrow-width: 0.875em;
$vpm-tooltip--arrow-height: 0.6em;

$vpm-tooltip--border-radius: 2px;
$vpm-tooltip--padding: 0.45em 0.75em;
$vpm-tooltip--z-index: 99;
```

## Caveats

The library makes use of `calc()`, and thus [will not work in IE8, Opera Mini, or earlier Android browsers](http://caniuse.com/calc). (A pull request that safely eliminates the `calc()` requirement would be [happily accepted](https://github.com/vanpattenmedia/vpm-tooltips/pulls)!)

Placing your tooltip text in the data attribute alone is _not sufficient for accessibility_. You might wish to set an `aria-label` attribute on your element, or use another recommended best practice to make sure you're accomomdating all users.

## Acknowledgements

This method of inserting tooltips was inspired by the [Daniel-Hug/tooltips](https://github.com/Daniel-Hug/tooltips) library.

## License

**Copyright (c) 2016 [Van Patten Media Inc.](https://www.vanpattenmedia.com/) All rights reserved.**

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

*   Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
*   Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
*   Neither the name of the organization nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
