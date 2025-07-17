origin [nginx_proxy](https://github.com/reiz/nginx_proxy)

苦于需要控制内网服务器访问受限的公网资源，最小化管控。

### build & run
build 
```
docker build -t nginx_proxy .
```
run
```
docker run -d -p 8888:8888 \
-v ${PWD}/nginx_allowlist.conf:/usr/local/nginx/conf/nginx.conf \
nginx_proxy
```
use proxy
```
export HTTP_PROXY=http://your_host_ip:8888
export HTTPS_PROXY=http://your_host_ip:8888
export http_proxy=http://your_host_ip:8888
export https_proxy=http://your_host_ip:8888

curl -v http://www.google.com

```

todo 访问来源ip做控制呢？
ip+端口模式的代理呢？
