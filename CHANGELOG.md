# Change Log

All notable changes to the "Paste JSON as Code (Refresh)" extension will be documented in this file.

## 1.0.21 - 2023-07-12

* 支持 json 转 YYModel
* 支持带注释的 json

## 1.0.2 - 2022-05-17

* Fixes a bug on switching target language for C#.

## 1.0.1 - 2022-05-09

* Update `README.md` and `CHANGELOG.md`.
* Add `System.Text.Json` support for C# target language
  * This also support .NET 6's `DateOnly` and `TimeOnly` types
* Add `quicktype.pickCsharpTargetLanguage` setting for choosing one of the following type:
  * `System.Text.Json`
  * `Newtonsoft.Json`
* Use VS Code extension [Data Storage APIs](https://code.visualstudio.com/api/extension-capabilities/common-capabilities#data-storage) (`workspaceState`) instead of using `node-persist` module
* Minor bug fixes

## 0.1.1 - 2021-05-28

* Update README.md
* Update npm packages & fixes `npm audit` issues

    ```sh
    npm i node-persist@3 quicktype-core typescript@4
    npm i -D @types/node-persist@3 @types/node@14 esbuild
    npm audit fix
    ```

## 0.1.0 - 2021-05-28

* Initial version
  * This version is based on commit `c002e41919ccb60aada85b8f00399f59f2dc8358` from https://github.com/quicktype/quicktype-vscode
* devDependencies
  * Upgrade `vsce` and `vscode` package to the latest version
* Publishing
  * Use `esbuild-watch` for default build task (`tasks.json`)
* Bundling Extensions
  * [Bundling Extensions](https://code.visualstudio.com/api/working-with-extensions/bundling-extension) using [esbuild](https://github.com/evanw/esbuild)
  * Ignore `node_modules` from publish to VSCode Marketplace (`.vscodeignore`)
* Git
  * Ignore `.vscode-test` from git (`.gitignore`)
