# AAPanel-Docker
<b>Changelog: </b>
- 08/03/2021: AAPanel + Docker Composer
- 15/07/2023: Update new docker image, fix error "OpenSSL_add_all_algorithms"

<b>Infomation: </b>
- AAPanel homepage: https://www.aapanel.com
- Docker source: https://hub.docker.com/r/aapanel/aapanel
- Default installation entry:aapanel => exp: http://localhost:21780/aapanel
- Default username: aapanel
- Default password: aapanel123

<b>Ports:</b>
- Control Panel: 8888
- Phpmyadmin: 888
- Redis Service: 6379

## PHP 配置
```shell
# 0. Start AAPanel
docker-compose up
# 1. 安装 php fileinfo 扩展 (php 7.4), 设置 limit timeout 为 1000
# 2. 访问 AAPanel
http://localhost:21780/aapanel
# 3. 在 AAPanel 中添加站点 shop.localhost
# 4. 设置 shop.localhost 的根目录为 /www/wwwroot/hd5.2.1
# 5. 设置属主机 host 文件，添加 shop.localhost
sudo vim /etc/hosts
127.0.0.1 shop.localhost
# 6. 安装站点
http://shop.localhost:21080/install.php
# 7. 访问后台
http://shop.localhost:21080/shop
```
前端: 小程序-H5打包
```shell
xcx-H5
# 配置文件
# xcx-H5/common/js/config.js
# uniapp HBuilderX 打包
# uni-app 打包
```

前端：PC订货端打包
```shell
web_os
# 配置文件
# web_os/plugins/config.js
# node version v12.0.0
npm run build
```

后端：PC 管理端打包
```shell
mshop_os
# 配置文件
# mshop_os/common/js/config.js
# uniapp HBuilderX 打包
# uni-app 打包
```

后端：PC管理端配置
```shell
# dev/aapanel-docker 目录启动环境
docker-compose up 
# 1. php 7.4 安装 fileinfo 扩展
# 2. mysql 修改root密码
# 3. 安装 niushop
http://nshop.localhost:21080/install.php/index/index?step=3
# 4. 访问首页
http://nshop.zxeg.top/shop/index/index.html
```