# eslint-config-greenroom

> Some opinionated style & type rules built on top of [eslint-config-standard-typescript-prettier](https://github.com/nfour/eslint-config-standard-typescript-prettier)
> 
> See [./.eslintrc.js](./.eslintrc.js)

## Install

Install it.

```bash
pnpm add -D eslint-config-greenroom
```

Wire it up.

```bash
echo "module.exports = require('eslint-config-greenroom')" > .eslintrc.js

# OR with react rules...

echo "module.exports = require('eslint-config-greenroom/.eslintrc.react')" > .eslintrc.js
```

Configure `.prettierrc.js` with something like:

```js
module.exports = {
  ...require('eslint-config-greenroom/.prettierrc'),
  semi: false,
}
```

Done.

## How it works

Thanks to `require('@rushstack/eslint-patch/modern-module-resolution');`, plugins can be included relative to the configs, not the consuming project, so you don't need to install any eslint plugins/config peer dependencies.