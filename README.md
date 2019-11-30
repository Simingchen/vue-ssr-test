## vue 的服务端渲染

1. 关键在于 server.js , 引入的几个 webpack 配置是为了生成 vue-ssr-client-manifest.json ， vue-ssr-server-bundle.json。
2. 实际在使用的时候其实是还是应用 dist 里面的文件，这两个 json 文件是告诉服务器需要引用哪一块 js 项目模块（比如订单模块页），然后抽出来的那部分引入到 server.js。
3. 根据 koa （或express）服务器渲染出来。

### vue-ssr-base项目
基于开发项目的修改，使前端部分完成文件打包

