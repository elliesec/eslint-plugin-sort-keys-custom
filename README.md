# eslint-plugin-sort-keys-custom

An ESLint rule that allows a customised sort order to be specified for object keys with an autofix available. Forked from [eslint-plugin-sort-keys-fix](https://github.com/leo-buneev/eslint-plugin-sort-keys-fix#readme).

## Installation

You'll first need to install [ESLint](http://eslint.org):

```
$ npm i eslint --save-dev
```

Next, install `eslint-plugin-sort-keys-custom`:

```
$ npm install eslint-plugin-sort-keys-custom --save-dev
```

**Note:** If you installed ESLint globally (using the `-g` flag) then you must also install `eslint-plugin-sort-keys-custom` globally.

## Usage

Add `sort-keys-custom` to the plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix:

```json
{
    "plugins": ["sort-keys-custom"]
}
```

Then add sort-keys-custom rule under the rules section.

```json
{
    "rules": {
        "sort-keys-custom/sort-keys-custom": "warn"
    }
}
```

Often it makes sense to enable `sort-keys-custom` only for certain files/directories. For cases like that, use override key of eslint config:

```jsonc
{
    "rules": {
        // ...
    },
    "overrides": [
        {
            "files": ["src/alphabetical.js", "bin/*.js", "lib/*.js"],
            "rules": {
                "sort-keys-custom/sort-keys-custom": "warn"
            }
        }
    ]
}
```

## Rule configuration

For available config options, see [official sort-keys reference](https://eslint.org/docs/rules/sort-keys#require-object-keys-to-be-sorted-sort-keys). All options supported by `sort-keys`, besides `minKeys`, are supported by `sort-keys-custom`.
