# @swivel-finance/eslint-config
ESLint config for @swivel-finance.

## Installation
To install this configuration, run
```
npx install-peerdeps --dev @swivel-finance/eslint-config
```
and add it to the `extends` field of your `.eslintrc` file:
```json
{
    "root": true,
    "extends": ["@swivel-finance"]
}
```

## Usage
Lint your project as usual, e.g. `npx eslint "src/**" --fix`

## Configuration

### Setting a custom `tsconfig.json`
You can customize the `tsconfig.json` file which the parser uses for analyzing and linting your project by setting it in your `.eslintrc` file:
```json
{
    "root": true,
    "extends": ["@swivel-finance"],
    "parserOptions": {
        "project": ["./src/tsconfig.build.json"]
    }
}
```
The default value is `./tsconfig.json`.

### Customizing rules
You can customize rules by adding them to the `rules` field of your `.eslintrc` file:
```json
{
    "root": true,
    "extends": ["@swivel-finance"],
    "parserOptions": {
        "project": ["./src/tsconfig.build.json"]
    },
    "rules": {
        "no-var": "off",
        "quotes": [
            "error",
            "single"
        ]
    }
}
```
