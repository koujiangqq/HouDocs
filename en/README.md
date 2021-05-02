## HouDocs

> A magical documentation site generator base on docsify.

## What it is

HouDocs generates your documentation website on the fly. Unlike GitBook, it does not generate static html files. Instead, it smartly loads and parses your Markdown files and displays them as a website. To start using it, all you need to do is create an `index.html` and [deploy it on GitHub Pages](deploy.md).

See the [Quick start](quickstart.md) guide for more details.

### Demo
* [https://docs.ulmt.com/](https://docs.ulmt.com/)


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

### Special thanks
* the developer of docsify(cinwell)


### Donate
Please consider donating if you think docsify is helpful to you or that my work is valuable. I am happy if you can help me buy a cup of coffee. 
* [https://pay.ulmt.com/](https://pay.ulmt.com/)
