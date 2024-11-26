# 验证安装
docker -v
docker-compose -v

# Linux 快速脚本 milvus
cd userfiles

# pgvector 版本(测试推荐，简单快捷)
curl -o docker-compose.yml https://raw.githubusercontent.com/labring/FastGPT/main/files/docker/docker-compose-pgvector.yml

# milvus 版本
curl -o docker-compose.yml https://raw.githubusercontent.com/labring/FastGPT/main/files/docker/docker-compose-milvus.yml

# zilliz 版本
curl -o docker-compose.yml https://raw.githubusercontent.com/labring/FastGPT/main/files/docker/docker-compose-zilliz.yml


# 启动容器
docker-compose up -d

# 等待10s，OneAPI第一次总是要重启几次才能连上Mysql

sleep 10
# 重启一次oneapi(由于OneAPI的默认Key有点问题，不重启的话会提示找不到渠道，临时手动重启一次解决，等待作者修复)
docker restart oneapi

docker-compose down

docker-compose up -d

ifconfig

http://172.18.0.1:11434