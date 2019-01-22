#Typescript

[Javascript Reference](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference)

## Debugging in VS Code using launch.json - Angular Projects

Add to .vscode -> launch.json

```{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "ng serve",
            "type": "chrome",
            "request": "launch",
            "url": "http://localhost:4200/#",
            "webRoot": "${workspaceRoot}"
          },
          {
            "name": "ng test",
            "type": "chrome",
            "request": "launch",
            "url": "http://localhost:9876/debug.html",
            "webRoot": "${workspaceRoot}"
          },
          {
            "name": "ng e2e",
            "type": "node",
            "request": "launch",
            "program": "${workspaceRoot}/node_modules/protractor/bin/protractor",
            "protocol": "inspector",
            "args": ["${workspaceRoot}/protractor.conf.js"]
          }
    ]
}
```
