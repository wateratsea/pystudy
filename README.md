# pystudy

python study repository

## how to install

1. download python embeded

> wsl get https://www.python.org/ftp/python/3.9.8/python-3.9.8-embed-amd64.zip

1. extract all files from compressed file

> wsl unzip ./python-3.9.8-embed-amd64.zip ./python

1. setting.json

```json:setting.json
{
    "terminal.integrated.env.windows": {
        "path": "${env:PATH};${workspaceFolder}\\python;${workspaceFolder}\\python\\Scrfipts;"
    },
    "python.pythonPath": "${workspaceFolder}\\python\\python.exe"
}
```

1. launch.json

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