# @cbschuld/prettier-config

My personal [prettier](https://prettier.io/) config - format influenced by [standardjs.com](standardjs.com)

## Installation

```sh
npm install --save-dev @cbschuld/prettier-config
```

Next, make sure you edit your `package.json` file by adding the reference for `prettier`:
```json
{
  // ...
  "prettier": "@cbschuld/prettier-config"
}
```

## Notes on VSCODE

To really enable VS CODE to work well with this configuration make sure you install both [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) and [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint).

Next, create a `settings.json` file in the `.vscode` root path of your project as follows.  (_Please note: this example contains additional settings I personally enjoy - you can ignore those_)
```json
{
  "editor.formatOnSave": true, // Tell VSCode to format files on save
  "editor.defaultFormatter": "esbenp.prettier-vscode", // Tell VSCode to use Prettier as default file formatter
  "editor.formatOnPaste": false,
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "files.exclude": {
    "node_modules/": true,
    "*/node_modules/": true,
    "**/node_modules/": true,
    "*/.serverless/": true,
    "**/.serverless/": true,
    "*/.webpack/": true,
    "**/.webpack/": true
  },
  "prettier.printWidth": 100,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "eslint.validate": ["react", "html", "javascript", "typescript"]
}

````