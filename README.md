origin [nginx_proxy](https://github.com/reiz/nginx_proxy)

苦于需要控制内网服务器访问受限的公网资源，最小化管控。

### build & run

```
docker compose up -d --build
```
使用出局代理
```
export HTTP_PROXY=http://your_host_ip:8888
export HTTPS_PROXY=http://your_host_ip:8888
export http_proxy=http://your_host_ip:8888
export https_proxy=http://your_host_ip:8888

curl -v http://www.google.com

```

todo 访问来源ip做控制呢？
ip+端口模式的代理呢？
集群高可用？
