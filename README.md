# pystudy
python study repository

## how to install

ダウンロード

https://www.python.org/ftp/python/3.9.8/python-3.9.8-embed-amd64.zip

- setting.json

```json:setting.json
{
    "terminal.integrated.env.windows": {
        "path": "${env:PATH};${workspaceFolder}\\python;${workspaceFolder}\\python\\Scrfipts;"
    },
    "python.pythonPath": "${workspaceFolder}\\python\\python.exe"
}
```

- launch.json

```json:launch.json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python: Current File (Integrated Terminal)",
            "type": "python",
            "request": "launch",
            "program": "${file}",
            "console": "integratedTerminal",
            "cwd": "${fileDirname}"
        }
    ]
}
```