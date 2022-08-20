# Git配置clash http代理

## Windows

### 命令

`git config --global http.proxy protocol://127.0.0.1:7890`

### 文件配置

Git的全局配置文件位于

`C:\Users\username\.gitconfig`

我这边使用的是clash作为代理软件，它的http代理为`http://127.0.0.1:7890`它的socks5代理为`socks5://127.0.0.1:7891`

打开后，在最后一行加入

```gitconfig
[http]
	proxy = http://127.0.0.1:7890
```

或者

```.gitconfig
[http]
	proxy = sock5://127.0.0.1:7891
```

然后`ctrl+s`保存，就可以了



以后我们到git上克隆仓库，速度就可以快很多了

> 链接要是https:开头的才行

![image-20220816100026190](https://static.meowrain.cn/i/2022/08/16/t2wrmx-3.png)



## Linux

### 命令

同上

### 文件配置

在`~`下创建`.gitconfig`

添加

打开后，在最后一行加入

```gitconfig
[http]
	proxy = http://127.0.0.1:7890
```

或者

```.gitconfig
[http]
	proxy = sock5://127.0.0.1:7891
```

用vim保存后，启动clash，在clone就会快很多了



> 注：设置全局git http代理后，在关闭clash后会无法克隆仓库。注意每次克隆前打开clash