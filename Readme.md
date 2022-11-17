## Mono Dev Container
This repo contains Mono dev container environment for basic setup.
It contains
- mono
- node
- mono-xps - for running asp.net application.

## How to
Drop .devcontainer and .vscode folder into your project. Re-Open project in container and run the app with F5
You might need to adjust `"cwd": "${workspaceRoot}"` to point your project root folder.
