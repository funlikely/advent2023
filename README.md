# advent2023
advent of code? Advent of code:



# Steps to make basic project
1 stack new advent2023
2 cd advent2023
3 stack build
4 Modify stack.yaml to include

resolver: ghc-9.2.5

5 Modify launch.json to include

```
        {
            "type": "ghc",
            "request": "launch",
            "name": "haskell(stack)",
            "internalConsoleOptions": "openOnSessionStart",
            "workspace": "${workspaceFolder}",
            "startup": "${workspaceFolder}/app/Main.hs",
            "startupFunc": "",
            "startupArgs": "",
            "stopOnEntry": false,
            "mainArgs": "",
            "ghciPrompt": "H>>= ",
            "ghciInitialPrompt": "> ",
            "ghciCmd": "stack ghci --with-ghc=ghci-dap --test --no-load --no-build --main-is TARGET",
            "ghciEnv": {},
            "logFile": "${workspaceFolder}/.vscode/phoityne.log",
            "logLevel": "WARNING",
            "forceInspect": false
        }
```

F7 - build
