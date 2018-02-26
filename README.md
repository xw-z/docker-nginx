
### 网站根目录
```
/var/www/html
```

### 设置容器日志大小和保留个数
docker run增加如下参数，限制生成的json.log单个文件大小和保留文件个数：
```
--log-opt max-size=10m --log-opt max-file=5
```
