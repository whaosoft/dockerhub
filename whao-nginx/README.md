# whao-nginx
支持tcp udp的docker nginx

暂时发个cent7 对应nginx 1.20.0的

```
demo
docker run --name x-nginx -d -p 6665:6665 -p 8088:8088/udp -p 80:80 -v /xx/nginx.conf:/usr/local/nginx/conf/nginx.conf -v /xx/logs:/usr/local/nginx/logs   whaosoft/whao-nginx:1.20.0
```
