## 修改默认中间件配置

ThinkKoa框架默认加载了logger、error、payload、router、http、static、controller等常用的中间件，这些中间件的配置在项目中未重新定义的时候，都遵循的默认配置，我们可以根据项目的实际情况进行修改。

这里以静态资源中间件`static`举例： 

修改项目中间件配置  src/config/middleware.js

```js
/**
 * Middleware config
 * @return
 */
module.exports = {
    list: [], //加载的中间件列表
    config: {
        static: { //重新定义static中间件配置
            cache: false //关闭静态资源缓存
        }
    }
};

```

具体的中间件配置项请参考各个中间件说明，[ThinkKoa中间件列表](/index/doc/plugin.jhtml)