# BMO部署说明

## 项目地址
输入命令

    https://github.com/mozilla-bteam/bmo.git
将项目clone到本地

## 启动说明
以下文件均在刚刚clone到本地的项目下

### docker-compose.yml 文件更改说明：

+ 添加外部访问端口

  进入到项目下，给bmo-web.vm容器添加外界访问端口

    ports:
      - "80:8000"
  其中容器内部监听端口为 ` ../Dockerfile` 中的 `ENV PORT=8000` 项定义。

+ 更改重定向地址

  更改 bmo-web.vm 容器的environment 的BMO_urlbase项
  
  将其中的域名，改为部署该应用的主机地址
  
### 启动

输入命令：
 
     docker-comose up
     
### 访问
  
输入：

http://yourid/

即可访问
