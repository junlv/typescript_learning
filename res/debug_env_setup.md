# 调试环境搭建 


学习使用typescript过程中 我使用Visual Studio Code 来作为调试工具,VS Code调试单个TS文件非常方便

## 配置调试环境

 1安装Visual Studio Code

 2 打开命令行,在工程目录下 npm i ts-node typescript tsc -D

 3 选中工具栏debug标签 添加调试配置文件

添加调试信息如下
```json
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "ts:debug",
            "type": "node",
            "request": "launch",
            "args": ["-r", "ts-node/register", "${relativeFile}"],
          }
    ]
}
```

该配置信息针对单个ts文件调试