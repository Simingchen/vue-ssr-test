## vue 的服务端渲染

1. 关键在于server.js, 引入的几个webpack配置是为了生成 vue-ssr-client-manifest.json，vue-ssr-server-bundle.json。
2. 实际在使用的时候其实是还是应用dist里面的文件，这两个json文件是告诉服务器需要引用哪一块文件dist文件夹里面的js项目模块（比如订单模块页），然后抽出来的那部分引入到server.js
3. 根据 koa （或express）服务器渲染出来
