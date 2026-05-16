# 起源AI - New API 部署信息
# Server: 111.92.240.250 (Debian 12, 8GB/100G)

## Docker
docker run --name new-api -d --restart always \
  -p 127.0.0.1:3000:3000 \
  -e TZ=Asia/Shanghai \
  -v /opt/new-api/data:/data \
  calciumion/new-api:latest

## Admin
- 用户名: root
- 密码: wasyyfv2015

## 品牌配置
- 系统名称: 起源AI
- Logo: https://api2.mcorgai.com/static/logo.jpg
- Logo 文件路径(服务器): /var/www/html/logo.jpg
- CF SSL: Flexible 模式

## Nginx
- 配置文件: /etc/nginx/sites-available/new-api
- 静态文件: /var/www/html/
- 反代: api2.mcorgai.com -> 127.0.0.1:3000

## 数据
- SQLite: /opt/new-api/data/one-api.db
