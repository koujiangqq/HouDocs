# 快速开始
下载好HouDocs后，可以看到 `./docs` 目录下创建的几个文件

- `index.html` 入口文件
- `README.md` 会做为主页内容渲染
- `.nojekyll` 用于阻止 GitHub Pages 会忽略掉下划线开头的文件
- `.sw.js`  serviceWorker文件,离线状态下网站正常运行

直接编辑 `docs/README.md` 就能更新网站内容，当然也可以[写多个页面](zh-cn/more-pages.md)。

## 预览网站

将文档发布到Apache和Nginx的支持html服务器的环境下实时的预览。

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



