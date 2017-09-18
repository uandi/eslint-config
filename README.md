# eslint-config-uandi

This package provides u+i's base JS .eslintrc as an extensible shared config.

## Install

Install via npm:

Install the correct versions of each package, which are listed by the command:

```sh
npm info "@uandi/eslint-config-uandi@latest" peerDependencies
```

Linux/OSX users can run

```sh
(
    export PKG="@uandi/eslint-config-uandi";
    npm info "$PKG@latest" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG@latest"
)
```

Which produces and runs a command like:

```sh
npm install --save dev eslint-config-uandi eslint@^#.#.# eslint-plugin-import@^#.#.#
```

Windows users can either install all the peer dependencies manually, or use the [install-peerdeps](https://github.com/nathanhleung/install-peerdeps) cli tool.

```sh
npm install -g install-peerdeps
install-peerdeps --dev eslint-config-uandi
```

## Usage

### eslint-config-uandi

Our configuration contains all of our ESLint rules, including ECMAScript 6+. It requires `eslint` and `eslint-plugin-import`.

Add `"extends": "@uandi/eslint-config-uandi"` to your .eslintrc

### eslint-config-uandi/legacy

Lints ES5 and below. Requires `eslint` and `eslint-plugin-import`.

Add `"extends": "@uandi/eslint-config-uandi/legacy"` to your .eslintrc
