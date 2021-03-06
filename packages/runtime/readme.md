# `@mdx-js/runtime`

[![Build Status][build-badge]][build]
[![lerna][lerna-badge]][lerna]
[![Join the community on Spectrum][spectrum-badge]][spectrum]

Parse and render [MDX][] in a runtime environment.

> :warning: **warning**: this is not the preferred way to use MDX since it
> introduces a substantial amount of overhead and dramatically increases
> bundle sizes.
> It should also not be used with user input that isn’t sandboxed.

## Installation

[npm][]:

```sh
npm i -S @mdx-js/runtime
```

## Usage

```jsx
import React from 'react'
import MDX from '@mdx-js/runtime'

const components = {
  h1: props => <h1 style={{ color: 'tomato' }} {...props} />
}

const mdx = '# Hello, world!'

export default () => (
  <MDX components={components}>{mdx}</MDX>
)
```

## Contribute

See [`contributing.md` in `mdx-js/mdx`][contributing] for ways to get started.

This organisation has a [Code of Conduct][coc].
By interacting with this repository, organisation, or community you agree to
abide by its terms.

## License

[MIT][] © [Compositor][] and [ZEIT][]

<!-- Definitions -->

[build]: https://travis-ci.org/mdx-js/mdx

[build-badge]: https://travis-ci.org/mdx-js/mdx.svg?branch=master

[lerna]: https://lernajs.io/

[lerna-badge]: https://img.shields.io/badge/maintained%20with-lerna-cc00ff.svg

[spectrum]: https://spectrum.chat/mdx

[spectrum-badge]: https://withspectrum.github.io/badge/badge.svg

[contributing]: https://github.com/mdx-js/mdx/blob/master/contributing.md

[coc]: https://github.com/mdx-js/mdx/blob/master/code-of-conduct.md

[mit]: license

[compositor]: https://compositor.io

[zeit]: https://zeit.co

[mdx]: https://github.com/mdx-js/mdx

[npm]: https://docs.npmjs.com/cli/install
