# Development Notes

1. Build & Run

    ```sh
    git clone https://github.com/doggy8088/quicktype-vscode-refresh.git
    cd quicktype-vscode-refresh
    npm install
    code .

    # Hit F5 to run
    ```

2. Update `quicktype` source code

    > Use `Node 8.x` and `Ubuntu` to build this project

    ```sh
    git clone https://github.com/doggy8088/quicktype.git -b CSharp-SystemTextJson
    cd quicktype
    npm install --ignore-scripts # Install dependencies
    npm install -g typescript    # Install typescript globally
    tsc --project src/cli        # Rebuild
    node dist/cli/index.js       # Run
    npm run build
    npm run pub
    ```

    [![Build status](https://dev.azure.com/willh/quicktype/_apis/build/status/quicktype-CI)](https://dev.azure.com/willh/quicktype/_build/latest?definitionId=69)

    I also have a [quicktype-csharp-demo](https://github.com/doggy8088/quicktype-csharp-demo) repo that is for testing the recent implementation of `System.Text.Json` support.
