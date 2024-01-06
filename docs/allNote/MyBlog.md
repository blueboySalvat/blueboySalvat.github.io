# 我为什么需要一个Blog
- 我想体验一次自己建站的感觉。
- 我想在上面做一下“我的关于”。
- 发布一点我写好的文章。

# 定位
- 发布一些在 obsidian中已经成熟完善的笔记。

# 建站之路

- npm是什么
NPM是随同NodeJS一起安装的包管理工具，能解决NodeJS代码部署上的很多问题，常见的使用场景有以下几种：
	- 允许用户从NPM服务器下载别人编写的第三方包到本地使用。
	- 允许用户从NPM服务器下载并安装别人编写的命令行程序到本地使用。
	- 允许用户将自己编写的包或命令行程序上传到NPM服务器供别人使用。

# 安装 git
苹果系统下可以直接在“终端”进行安装
输入 git --version（查看git版本命令）它就会自动弹窗，进行安装即可
# 安装nodejs
- 下载地址：[Node.js](https://nodejs.org/en)
可以下载 xx. Xx. Xx LTS 版本（**长期支持版本**，重点在于稳定性和安全性）
- 更新 npm 到最新版本（新版的 nodejs 已经集成 npm）
```
sudo npm install npm -g
```

# 安装 docsify-cli 工具
- 用于创建及本地预览文档网站
```
npm i docsify-cli -g
```
- 初始化
```
docsify init ./docs
```
docs 文件夹基本目录结构：
```
wangwenpeng@AppleBook ~ % pwd
/Users/wangwenpeng
wangwenpeng@AppleBook ~ % ls
Applications Movies
Applications (Parallels) Music
Desktop Parallels
Documents Pictures
Downloads Public
Library docs
wangwenpeng@AppleBook ~ % ls docs
README.md index.html
```
README.md  
index.html -入口文件
- 启动 docsify
```
wangwenpeng@AppleBook ~ % sudo docsify serve ./docs

Password:

  

Serving /Users/wangwenpeng/docs now.

Listening at http://localhost:60304
```



参考文章：
[docsify](https://docsify.js.org/#/zh-cn/quickstart?id=初始化项目)
[3 使用 docsify 构建文档](https://notebook.js.org/#/Project/Docsify/docsifyNotes?id=_3-使用-docsify-构建文档)
[部署](https://docsify.js.org/#/zh-cn/deploy?id=github-pages)