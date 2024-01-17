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
- Website domain: http://rewrite.localhost:21080/

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
