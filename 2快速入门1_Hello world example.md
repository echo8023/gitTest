# Hello world example

**创建一个名为app的快速实例**

本质上，下面嵌入是您可以创建的最简单的Express应用程序。它是一个单一文件的应用程序-如果您使用Express生成器，则不会得到,它为具有各种用途的大量JavaScript文件，Jade模板和子目录为完整的应用程序创建了脚手架.

```
//mynote: 入口文件中(例如:index.js/app.js),看入口文件是哪个,就看package.json中的main:右边的内容 ??????
const express = require('express') //对象的引用地址是不变的,所以可以用const定义
const app = express()

app.get('/', (req, res) => res.send('Hello World!'))

app.listen(3000, () => console.log('Example app listening on port 3000!'))
```

该应用程序启动服务器，并在端口3000上侦听连接。该应用程序以“ Hello World！”响应，以请求根URL（/）或路由。对于其他所有路径，它将以404 Not Found响应。

// 上面的示例实际上是一个正常工作的服务器：继续并单击显示的URL。您会在页面上获得实时日志的响应，并且您所做的任何更改都会实时反映出来。它由RunKit提供支持，RunKit提供了一个交互式JavaScript游乐场，该游乐场连接到在Web浏览器中运行的完整Node环境。以下是在本地计算机上运行同一应用程序的说明。

RunKit是不属于Express项目的第三方服务。

### Running Locally (本地运行)

首先创建一个名为myapp的目录，切换到该目录并运行npm init。然后按照安装指南将express安装为依赖项。

在myapp目录中，创建一个名为app.js (mynote: 或者index,js--入口文件) 的文件，并复制上面示例中的代码。

 req（请求）和res（响应）与Node提供的对象完全相同，因此您可以调用req.pipe（），req.on（'data'，callback）以及无需Express即可进行的其他任何操作。

使用以下命令运行该应用程序:

```sh
$ node app.js
```

然后，在浏览器中加载http://localhost:3000/以查看输出。