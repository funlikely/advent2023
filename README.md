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


Oy, Haskell on Windows has landed me in dependency h*ll. Possibly problems from installing the -dap extension.
But currently I see 

```
 ghci-dap --version
[DAP][INFO] start ghci-dap-0.0.20.0.
The Glorious Glasgow Haskell Compilation System, version 9.2.6
```

And I looked up on stackage.org that
LTS 20.12 for ghc-9.2.6, published 9 months ago

So I set in stack.yaml:

```
resolver:  lts-20.12
```

and now I can use F9 to set a breakpoint and F5 to hit the breakpoint.

Now the goal is to see about starting to add some non-hello-world code to the project.
