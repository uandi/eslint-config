# eslint-config-uandi

This package provides u+i's base JS .eslintrc as an extensible shared config.

## Install

Install via npm:

Install the correct versions of each package, which are listed by the command:

```sh
npm info "@uandi/eslint-config@latest" peerDependencies
```

Linux/OSX users can run

```sh
(
    export PKG="@uandi/eslint-config";
    npm info "$PKG@latest" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG@latest"
)
```

Which produces and runs a command like:

```sh
npm install --save dev @uandi/eslint-config eslint@^#.#.# eslint-plugin-import@^#.#.#
```

Windows users can either install all the peer dependencies manually, or use the [install-peerdeps](https://github.com/nathanhleung/install-peerdeps) cli tool.

```sh
npm install -g install-peerdeps
install-peerdeps --dev @uandi/eslint-config
```

## Usage

### @uandi/eslint-config

Our configuration contains all of our ESLint rules, including ECMAScript 6+. It requires `eslint` and `eslint-plugin-import`.

Add `"extends": "@uandi/eslint-config"` to your .eslintrc

### @uandi/eslint-config/legacy

Lints ES5 and below. Requires `eslint` and `eslint-plugin-import`.

Add `"extends": "@uandi/eslint-config/legacy"` to your .eslintrc

### @uandi/eslint-config/whitespace

Errors only on whitespace rules and sets all other rules to warning.

Add `"extends": "@uandi/eslint-config/whitespace"` to your .eslintrc
