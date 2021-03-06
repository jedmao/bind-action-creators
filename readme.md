# bind-action-creators

<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
[![GitHub Actions](https://github.com/jedmao/bind-action-creators/workflows/Node%20CI/badge.svg?event=push)](https://github.com/jedmao/bind-action-creators/actions)
[![codecov](https://img.shields.io/codecov/c/gh/jedmao/bind-action-creators?style=flat-square)](https://codecov.io/gh/jedmao/bind-action-creators)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg?style=flat-square)](http://commitizen.github.io/cz-cli/)
[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg?style=flat-square)](https://github.com/xojs/xo)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)
[![types: TypeScript](https://img.shields.io/npm/types/typescript?style=flat-square)](https://typescriptlang.org)
<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- markdownlint-disable commands-show-output -->

Turns an object whose values are action creators, into an object with the same
keys, but with every action creator wrapped into a dispatch call so they may be
invoked directly.

## Installation

```bash
npm install bind-action-creators
```

## Usage

```ts
import bindActionCreators = require('bind-action-creators')

const actionCreators = {
  fetchFoo: dispatch => Promise.resolve([]),
  fetchBar: dispatch => Promise.resolve([]),
}

const bound = bindActionCreators(actionCreators /*, dispatch */)
```

## Scripts

The following [npm scripts](https://docs.npmjs.com/misc/scripts) are made
available to you in the project root. You can run each of them with
`npm run <script-name>`.

### build

Runs the [TypeScript][] compiler.

### test

Runs [AVA][] in
[watch mode](https://github.com/avajs/ava/blob/master/docs/recipes/watch-mode.md),
which attempts to run only on changed files.

### cover

Runs [AVA][] with
[coverage](https://github.com/avajs/ava/blob/master/docs/recipes/code-coverage.md),
dumping coverage results in `./coverage` and showing a text summary in the
console output.

### commit

Runs [Commitizen](http://commitizen.github.io/cz-cli/) commit wizard, ensuring
that your commit messages conform to
[Conventional Commits](https://www.conventionalcommits.org/).

### Tips

Use the [`git commit`](https://git-scm.com/docs/git-commit) command directly
with the
[`-n`, `--no-verify` option](https://git-scm.com/docs/git-commit#Documentation/git-commit.txt--n)
to bypasses the pre-commit and commit-msg hooks.

[ava]: https://github.com/avajs/ava
[typescript]: http://www.typescriptlang.org/
