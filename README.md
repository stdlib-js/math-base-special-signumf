<!--

@license Apache-2.0

Copyright (c) 2020 The Stdlib Authors.

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

# Signum

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Signum][signum] function.

<section class="intro">

The [signum][signum] function is defined as

<!-- <equation class="equation" label="eq:signum_function" align="center" raw="\operatorname{sign}(x) := \begin{cases} -1 & \textrm{if}\ x < 0 \\ 0 & \textrm{if}\ x = 0 \\ 1 & \textrm{if}\ x > 0 \end{cases}" alt="Signum function"> -->

<div class="equation" align="center" data-raw-text="\operatorname{sign}(x) := \begin{cases} -1 &amp; \textrm{if}\ x &lt; 0 \\ 0 &amp; \textrm{if}\ x = 0 \\ 1 &amp; \textrm{if}\ x &gt; 0 \end{cases}" data-equation="eq:signum_function">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@4e38532a2ca3d2a641daa792a9c4c0fce3e749eb/lib/node_modules/@stdlib/math/base/special/signumf/docs/img/equation_signum_function.svg" alt="Signum function">
    <br>
</div>

<!-- </equation> -->

for any real number `x`.

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-signumf
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm` branch][esm-url].
-   If you are using Deno, visit the [`deno` branch][deno-url].
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd` branch][umd-url].

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

</section>

<section class="usage">

## Usage

```javascript
var signumf = require( '@stdlib/math-base-special-signumf' );
```

#### signumf( x )

Evaluates the [signum][signum] function for a single-precision floating-point number.

```javascript
var sign = signumf( -5.0 );
// returns -1

sign = signumf( 5.0 );
// returns 1

sign = signumf( -0.0 );
// returns -0

sign = signumf( 0.0 );
// returns 0

sign = signumf( NaN );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="notes">

## Notes

Table of results:

| Value   | Sign  |
| ------- | ----- |
| `x > 0` | `+1`  |
| `x < 0` | `-1`  |
| `0`     | `0`   |
| `-0`    | `-0`  |
| `NaN`   | `NaN` |

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var round = require( '@stdlib/math-base-special-round' );
var signumf = require( '@stdlib/math-base-special-signumf' );

var sign;
var x;
var i;

for ( i = 0; i < 100; i++ ) {
    x = round( randu()*100.0 ) - 50.0;
    sign = signumf( x );
    console.log( 'signum(%d) = %d', x, sign );
}
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->

* * *

<section class="c">

## C APIs

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- C usage documentation. -->

<section class="usage">

### Usage

```c
#include "stdlib/math/base/special/signumf.h"
```

#### stdlib_base_signumf( x )

Evaluates the [signum][signum] function for a single-precision floating-point number.

```c
float y = stdlib_base_signumf( -9.0f );
// returns -1.0f
```

The function accepts the following arguments:

-   **x**: `[in] float` input value.

```c
float stdlib_base_signumf( const float x );
```

</section>

<!-- /.usage -->

<!-- C API usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

</section>

<!-- /.notes -->

<!-- C API usage examples. -->

<section class="examples">

### Examples

```c
#include "stdlib/math/base/special/signumf.h"
#include <stdio.h>

int main() {
    float x[] = { 3.14f, -3.14f, 0.0f, 0.0f/0.0f };

    float y;
    int i;
    for ( i = 0; i < 4; i++ ) {
        y = stdlib_base_signumf( x[ i ] );
        printf( "signum(%f) = %f\n", x[ i ], y );
    }
}
```

</section>

<!-- /.examples -->

</section>

<!-- /.c -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/math/base/special/signum`][@stdlib/math/base/special/signum]</span><span class="delimiter">: </span><span class="description">evaluate the signum function for a double-precision floating-point number.</span>

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

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-signumf.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-signumf

[test-image]: https://github.com/stdlib-js/math-base-special-signumf/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/math-base-special-signumf/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-signumf/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-signumf?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-signumf.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-signumf/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-signumf/tree/deno
[umd-url]: https://github.com/stdlib-js/math-base-special-signumf/tree/umd
[esm-url]: https://github.com/stdlib-js/math-base-special-signumf/tree/esm
[branches-url]: https://github.com/stdlib-js/math-base-special-signumf/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-signumf/main/LICENSE

[signum]: http://en.wikipedia.org/wiki/Sign_function

<!-- <related-links> -->

[@stdlib/math/base/special/signum]: https://github.com/stdlib-js/math-base-special-signum

<!-- </related-links> -->

</section>

<!-- /.links -->
