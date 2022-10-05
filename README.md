# the-library
项目演示见[The Library](https://note.jyhao.top/pdf)

相关技能：
* nginx autoindex 
* ajax
* bootstrap 

重新编写nginx autoindex功能，实现在线图书馆功能。

nginx配置如下：
```
       location /books/ {
                root /data/;
                #add_header 'Access-Control-Allow-Origin' '*';
                autoindex on;
                autoindex_format json;
        }
        location /pdf {
                index index.html;
                alias /etc/nginx/html;
        }
```
