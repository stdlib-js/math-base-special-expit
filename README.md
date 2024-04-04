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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# expit

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Compute the [standard logistic][logistic-function] function.

<section class="intro">

The [standard logistic][logistic-function] function, also called the expit function, inverse logit, or sigmoid function, is defined as the [logistic][logistic-function] function with parameters (`k = 1`, `x0 = 0`, `L = 1`).

<!-- <equation class="equation" label="eq:expit_function" align="center" raw="\begin{aligned}\operatorname{expit}(x) &= \frac{1}{1+e^{-x}} \\ &= \frac{e^{x}}{e^{x}+1} \\ &= \frac{1}{2} + \frac{1}{2}\tanh\frac{x}{2} \end{aligned}" alt="Standard logistic function."> -->

```math
\begin{aligned}\mathop{\mathrm{expit}}(x) &= \frac{1}{1+e^{-x}} \\ &= \frac{e^{x}}{e^{x}+1} \\ &= \frac{1}{2} + \frac{1}{2}\tanh\frac{x}{2} \end{aligned}
```

<!-- <div class="equation" align="center" data-raw-text="\begin{aligned}\operatorname{expit}(x) &amp;= \frac{1}{1+e^{-x}} \\ &amp;= \frac{e^{x}}{e^{x}+1} \\ &amp;= \frac{1}{2} + \frac{1}{2}\tanh\frac{x}{2} \end{aligned}" data-equation="eq:expit_function">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@011d8b8e35ceb466ad31f5484e176ccaeaa087a2/lib/node_modules/@stdlib/math/base/special/expit/docs/img/equation_expit_function.svg" alt="Standard logistic function.">
    <br>
</div> -->

<!-- </equation> -->

</section>

<!-- /.intro -->



<section class="usage">

## Usage

```javascript
import expit from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-expit@deno/mod.js';
```
The previous example will load the latest bundled code from the deno branch. Alternatively, you may load a specific version by loading the file from one of the [tagged bundles](https://github.com/stdlib-js/math-base-special-expit/tags). For example,

```javascript
import expit from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-expit@v0.2.2-deno/mod.js';
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
import randu from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-base-randu@deno/mod.js';
import expit from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-expit@deno/mod.js';

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

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-expit.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-expit

[test-image]: https://github.com/stdlib-js/math-base-special-expit/actions/workflows/test.yml/badge.svg?branch=v0.2.2
[test-url]: https://github.com/stdlib-js/math-base-special-expit/actions/workflows/test.yml?query=branch:v0.2.2

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
[deno-readme]: https://github.com/stdlib-js/math-base-special-expit/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-special-expit/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-special-expit/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-special-expit/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-special-expit/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-special-expit/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-expit/main/LICENSE

[logistic-function]: https://en.wikipedia.org/wiki/Logistic_function

<!-- <related-links> -->

[@stdlib/math/base/special/exp]: https://github.com/stdlib-js/math-base-special-exp/tree/deno

[@stdlib/math/base/special/logit]: https://github.com/stdlib-js/math-base-special-logit/tree/deno

<!-- </related-links> -->

</section>

<!-- /.links -->
