<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

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

# expit

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Compute the [standard logistic][logistic-function] function.

<section class="intro">

The [standard logistic][logistic-function] function, also called the expit function, inverse logit, or sigmoid function, is defined as the [logistic][logistic-function] function with parameters (`k = 1`, `x0 = 0`, `L = 1`).

<!-- <equation class="equation" label="eq:expit_function" align="center" raw="\begin{aligned}\operatorname{expit}(x) &= \frac{1}{1+e^{-x}} \\ &= \frac{e^{x}}{e^{x}+1} \\ &= \frac{1}{2} + \frac{1}{2}\tanh\frac{x}{2} \end{aligned}" alt="Standard logistic function."> -->

```math
\begin{aligned}\operatorname{expit}(x) &= \frac{1}{1+e^{-x}} \\ &= \frac{e^{x}}{e^{x}+1} \\ &= \frac{1}{2} + \frac{1}{2}\tanh\frac{x}{2} \end{aligned}
```

<!-- <div class="equation" align="center" data-raw-text="\begin{aligned}\operatorname{expit}(x) &amp;= \frac{1}{1+e^{-x}} \\ &amp;= \frac{e^{x}}{e^{x}+1} \\ &amp;= \frac{1}{2} + \frac{1}{2}\tanh\frac{x}{2} \end{aligned}" data-equation="eq:expit_function">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@011d8b8e35ceb466ad31f5484e176ccaeaa087a2/lib/node_modules/@stdlib/math/base/special/expit/docs/img/equation_expit_function.svg" alt="Standard logistic function.">
    <br>
</div> -->

<!-- </equation> -->

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-expit
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
var expit = require( '@stdlib/math-base-special-expit' );
```

#### expit( x )

Computes the [standard logistic][logistic-function] function.

```javascript
var v = expit( 0.0 );
// returns ~0.5

v = expit( 1.0 );
// returns ~0.731

v = expit( -1.0 );
// returns ~0.269

v = expit( Infinity );
// returns 1.0

v = expit( NaN );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var randu = require( '@stdlib/random-base-randu' );
var expit = require( '@stdlib/math-base-special-expit' );

var x;
var i;

for ( i = 0; i < 100; i++ ) {
    x = randu();
    console.log( 'expit(%d) = %d', x, expit( x ) );
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
#include "stdlib/math/base/special/expit.h"
```

#### stdlib_base_expit( x )

Computes the [standard logistic][logistic-function] function.

```c
double out = stdlib_base_expit( 0.0 );
// returns ~0.5

out = stdlib_base_expit( 1.0 );
// returns ~0.731
```

The function accepts the following arguments:

-   **x**: `[in] double` input value.

```c
double stdlib_base_expit( const double x );
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
#include "stdlib/math/base/special/expit.h"
#include <stdlib.h>
#include <stdio.h>

int main() {
    double x;
    double v;
    int i;
    
    for ( i = 0; i < 100; i++ ) {
        x = (double)rand() / (double)RAND_MAX;
        v = stdlib_base_expit( x );
        printf( "expit(%lf) = %lf\n", x, v );
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

-   <span class="package-name">[`@stdlib/math-base/special/exp`][@stdlib/math/base/special/exp]</span><span class="delimiter">: </span><span class="description">natural exponential function.</span>
-   <span class="package-name">[`@stdlib/math-base/special/logit`][@stdlib/math/base/special/logit]</span><span class="delimiter">: </span><span class="description">logit function.</span>

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

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-expit.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-expit

[test-image]: https://github.com/stdlib-js/math-base-special-expit/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/math-base-special-expit/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-expit/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-expit?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-expit.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-expit/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-expit/tree/deno
[umd-url]: https://github.com/stdlib-js/math-base-special-expit/tree/umd
[esm-url]: https://github.com/stdlib-js/math-base-special-expit/tree/esm
[branches-url]: https://github.com/stdlib-js/math-base-special-expit/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-expit/main/LICENSE

[logistic-function]: https://en.wikipedia.org/wiki/Logistic_function

<!-- <related-links> -->

[@stdlib/math/base/special/exp]: https://github.com/stdlib-js/math-base-special-exp

[@stdlib/math/base/special/logit]: https://github.com/stdlib-js/math-base-special-logit

<!-- </related-links> -->

</section>

<!-- /.links -->
