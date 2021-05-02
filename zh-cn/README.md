## HouDocs

> 基于docsify的一个神奇的文档网站生成工具,只需要创建一个 index.html 就可以开始在线写文档

## 是什么

HouDocs 是一个动态生成文档网站的工具。不同于 GitBook、Hexo 的地方是它不会生成将 `.md` 转成 `.html` 文件，所有转换工作都是在运行时进行。

这将非常实用，如果只是需要快速的搭建一个小型的文档网站，或者不想因为生成的一堆 `.html` 文件“污染” commit 记录，只需要创建一个 `index.html` 就可以开始写文档而且直接[部署在 GitHub Pages](zh-cn/deploy.md)。

查看[快速开始](zh-cn/quickstart.md)了解详情。

### Demo
* [https://docs.ulmt.com/](https://docs.ulmt.com/)


### 特别感谢
* docsify的开发者cinwell


## 使用方法
* 获取最新HouDocs源代码放到站点根目录 


### 注意
Apache和Nginx环境下README.md文件无法访问，首页一直显示404解决方案
解决方法:

Apache:
修改网站配置文件，删除掉|README.md部分即可

```html
#DENY FILES
 <Files ~ (\.user.ini|\.htaccess|\.git|\.svn|\.project|LICENSE|README.md)$>
   Order allow,deny
   Deny from all
</Files>
```


nginx:
同样访问配置文件，修改这段代码，删掉|README.md就好了 
```html
location ~ ^/(\.user.ini|\.htaccess|\.git|\.svn|\.project|LICENSE|README.md
    {
        return 404;
   }
```

### 欢迎打赏
如果你觉得 HouDocs 对你有帮助，或者想对我微小的工作一点支持，欢迎打赏鼓励一下
* [https://pay.ulmt.com/](https://pay.ulmt.com/)
 