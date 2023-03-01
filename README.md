<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# ifthen

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> If a condition is truthy, invoke `x`; otherwise, invoke `y`.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

To use in Observable,

```javascript
ifthen = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/utils-if-then@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var ifthen = require( 'path/to/vendor/umd/utils-if-then/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/utils-if-then@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.ifthen;
})();
</script>
```

#### ifthen( bool, x, y )

If a condition is truthy, invokes `x`; otherwise, invokes `y`.

```javascript
function x() {
    return 1.0;
}

function y() {
    return -1.0;
}

var z = ifthen( true, x, y );
// returns 1.0

z = ifthen( false, x, y );
// returns -1.0
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   The function is similar to [`ifelse()`][@stdlib/utils/if-else], but allows deferred argument evaluation.

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-ceil@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/string-repeat@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/utils-if-then@umd/browser.js"></script>
<script type="text/javascript">
(function () {

var z;
var i;

function x() {
    return repeatString( 'BOOP', ceil( randu()*3.0 ) );
}

function y() {
    return repeatString( 'beep', ceil( randu()*5.0 ) );
}

for ( i = 0; i < 100; i++ ) {
    z = ifthen( randu() > 0.9, x, y );
    console.log( z );
}

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/utils-async/if-then`][@stdlib/utils/async/if-then]</span><span class="delimiter">: </span><span class="description">if a predicate function returns a truthy value, invoke `x`; otherwise, invoke `y`.</span>
-   <span class="package-name">[`@stdlib/utils-if-else`][@stdlib/utils/if-else]</span><span class="delimiter">: </span><span class="description">if a condition is truthy, return `x`; otherwise, return `y`.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/utils-if-then.svg
[npm-url]: https://npmjs.org/package/@stdlib/utils-if-then

[test-image]: https://github.com/stdlib-js/utils-if-then/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/utils-if-then/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/utils-if-then/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/utils-if-then?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/utils-if-then.svg
[dependencies-url]: https://david-dm.org/stdlib-js/utils-if-then/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/utils-if-then/tree/deno
[umd-url]: https://github.com/stdlib-js/utils-if-then/tree/umd
[esm-url]: https://github.com/stdlib-js/utils-if-then/tree/esm
[branches-url]: https://github.com/stdlib-js/utils-if-then/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/utils-if-then/main/LICENSE

<!-- <related-links> -->

[@stdlib/utils/async/if-then]: https://github.com/stdlib-js/utils-async-if-then/tree/umd

[@stdlib/utils/if-else]: https://github.com/stdlib-js/utils-if-else/tree/umd

<!-- </related-links> -->

</section>

<!-- /.links -->
