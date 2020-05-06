[![official JetBrains project](https://jb.gg/badges/official-flat-square.svg)](https://confluence.jetbrains.com/display/ALL/JetBrains+on+GitHub)

IntelliJ Platform SDK 文档
=======

欢迎来到 [IntelliJ Platform SDK 文档](https://intellij-sdk-docs-cn.github.io)页面的仓库。

## 报告 Bug
请通过提交一个 issue 到
[Github](https://github.com/intellij-sdk-docs-cn/intellij-sdk-docs-cn/issues) 来报告任何在文档或示例中找到的内容不一致、过时材料、外观问题与其他缺陷。

## 在本地运行站点
要 check out 并运行站点的本地副本，请按照以下步骤。

### 前置要求

*  确保你有
   安装
   [git 客户端](https://git-scm.com/downloads)

*  这个站点需要
   [Ruby 2.0](https://www.ruby-lang.org/) 或更高版本。
   按照官方 Ruby 语言的
   [下载](https://www.ruby-lang.org/en/downloads/)
   与
   [安装](https://www.ruby-lang.org/en/documentation/installation/)
   提示来获取 Ruby 以在你的机器上工作。
   
*  这个站点需要 [Jekyll](https://jekyllrb.com/)， 
   一个基于 Ruby 的站点生成框架。
   要安装 Jekyll，请参考它的
   [安装指导](https://jekyllrb.com/docs/installation/).
   **注意：** 如果你在使用 Windows，你可以在安装 Jekyll 期间面对一些特定发方面。
   参见这个[在 Windows 上运行 Jekyll 指南](https://jekyll-windows.juthilo.com/)来获取更多详情。
   
### Checking Out 站点仓库

要 check out 源代码，请运行以下命令：

```bash
git clone https://github.com/JetBrains/intellij-sdk-docs.git
```
   
### 初始化子模块

这个站点使用了 JetBrains 自定义的网页模板。
要在本地启用自定义模板，你需要初始化仓库子模块。
在 checkout 目录中运行以下命令。
 
```bash
git submodule update --init --remote
```

### 安装 Gems

为主仓库与子模块运行初始 checkout 后，运行 `bundle install` 来安装其他必要的 gems。

### 构建并预览
一套 Rake 任务，一个在 Ruby 上实现的类似于 Make 程序，提供了短命令来构建并在本地运行站点。 

#### 从源代码构建站点
 
*  确保你在项目的根目录
*  要构建静态站点内容，请运行
   ```bash
   rake build
   ```
   
#### 预览

*  要启动 web 服务器，请运行
    ```bash
    rake preview
    ```
*  在你的浏览器中
   打开地址
   [http://localhost:4000/intellij/sdk/docs/](http://localhost:4000/intellij/sdk/docs/)
   **注意:** 确保你没有在安装过程中改变默认 Jekyll 端口。


