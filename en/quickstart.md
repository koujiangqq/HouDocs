# Quick start

After download HouDocs, you can see the file list in the `./docs` subdirectory.

* `index.html` as the entry file
* `README.md` as the home page
* `.nojekyll` prevents GitHub Pages from ignoring files that begin with an underscore
* `.sw.js` serviceWorker文件,离线状态下网站正常运行

You can easily update the documentation in `./docs/README.md`, of course you can add [more pages](more-pages.md).

## Preview Docs
Publish documents to Apache and Nginx servers for real-time preview

### Notice
Apache and Nginx environments, and the family keeps showing the 404.
Solution:

Apache:
Modify the website configuration file and delete the part |README.md

```html
#DENY FILES
 <Files ~ (\.user.ini|\.htaccess|\.git|\.svn|\.project|LICENSE|README.md)$>
   Order allow,deny
   Deny from all
</Files>
```


nginx:
Modify the website configuration file and delete the part |README.md 
```html
location ~ ^/(\.user.ini|\.htaccess|\.git|\.svn|\.project|LICENSE|README.md
    {
        return 404;
   }
```
