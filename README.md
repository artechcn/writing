
## 安装docfx

从 [https://github.com/dotnet/docfx/releases](https://github.com/dotnet/docfx/releases) 下载并解压缩 docfx.zip，将其压缩到一个本地文件夹，并添加到PATH中，这样就可以在任何地方运行它


## 运行项目

执行命令：

```
docfx docfx_project\docfx.json --serve
```

然后在浏览器里面访问 [http://localhost:8080](http://localhost:8080) 就可以看到了。

如果8080端口号已被占用，后面加上 -p 端口号：

```
docfx docfx_project\docfx.json --serve --port 8081
```