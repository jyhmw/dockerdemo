# Docker Demo

一个极简的 Node.js Web Demo，零第三方依赖，使用 Docker 部署。

## 功能

- `/` —— 演示页面，展示容器信息（主机名、运行时长、请求数等）
- `/api/info` —— JSON 格式的运行信息
- `/healthz` —— 健康检查端点，返回 `ok`

## 本地运行（Docker）

```bash
# 构建镜像
docker build -t docker-demo .

# 运行容器（映射到宿主机 3000 端口，可自行修改）
docker run -d --name docker-demo -p 3000:3000 docker-demo
```

打开 http://localhost:3000 查看页面。

## 本地运行（无 Docker）

```bash
npm start   # 或 node server.js
```

环境变量 `PORT` 可自定义监听端口，默认 3000。
