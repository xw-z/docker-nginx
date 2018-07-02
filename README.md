
### 网站根目录
```
/var/nginx/html
```

### 设置容器日志大小和保留个数
docker run增加如下参数，限制生成的json.log单个文件大小和保留文件个数：
```
--log-opt max-size=10m --log-opt max-file=5
```

```
cid=`docker build --no-cache=true -t www.example.com .`
docker run -d --restart=always \
	-e VIRTUAL_HOST=www.example.com -e VIRTUAL_PORT=80 \
	--log-opt max-size=10m --log-opt max-file=5 \
	--name=www.example.com cid
```

