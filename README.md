# OpenAI-New API 镜像同步仓库

## 📋 项目简介

本仓库自动同步 [calciumion/new-api](https://hub.docker.com/r/calciumion/new-api) Docker 镜像到 GitHub Container Registry (GHCR)。

## 🚀 镜像信息

- **镜像地址**: `ghcr.io/bqizkm01918t/openai-new:latest`
- **镜像大小**: 68.4MB
- **源镜像**: `calciumion/new-api:latest`
- **同步频率**: 每日自动同步 (北京时间上午 10 点)
- **源镜像摘要**: calciumion/new-api@sha256:d9a10b4f0f45a16cafc16ed96ff116b8087373185b00e6e76b9d2a0334ba29b0
- **当前版本标签**: 20251101081118

## 📅 同步记录

| 同步时间 | 触发方式 | 版本标签 | 状态 |
|----------|----------|----------|------|
| 2025-11-01 08:11:21 UTC | 手动触发 | 20251101081118 | ✅ 成功 |

## 🔄 同步流程

1. 清理本地Docker缓存
2. 从 Docker Hub 强制拉取最新 `calciumion/new-api` 镜像
3. 创建带时间戳的唯一标签
4. 重新标记为 `ghcr.io/bqizkm01918t/openai-new`
5. 推送到 GitHub Container Registry
6. 验证镜像是否成功推送
7. 更新本 README 文件

## 📦 使用方法

### 使用 SQLite 数据库

```bash
# 使用SQLite
docker run --name new-api -d --restart always -p 3000:3000 -e TZ=Asia/Shanghai -v /home/ubuntu/data/new-api:/data ghcr.io/bqizkm01918t/openai-new:latest
```

### 使用特定版本

```bash
# 使用特定版本（推荐）
docker run --name new-api -d --restart always -p 3000:3000 -e TZ=Asia/Shanghai -v /home/ubuntu/data/new-api:/data ghcr.io/bqizkm01918t/openai-new:20251101081118
```

### Docker Compose

```yaml
version: '3'
services:
  openai-new:
    image: ghcr.io/bqizkm01918t/openai-new:latest
    container_name: new-api
    restart: always
    ports:
      - "3000:3000"
    environment:
      - TZ=Asia/Shanghai
    volumes:
      - /home/ubuntu/data/new-api:/data
```

## ⚙️ 配置说明

- **端口映射**: 容器内 3000 端口映射到主机 3000 端口
- **时区设置**: 设置为亚洲/上海时区
- **数据持久化**: 主机目录 `/home/ubuntu/data/new-api` 挂载到容器内 `/data` 目录
- **自动重启**: 容器异常退出时自动重启

## ⚠️ 注意事项

- 本镜像仅作同步用途，请勿用于生产环境
- 如需了解原始项目详情，请访问 [calciumion/new-api](https://hub.docker.com/r/calciumion/new-api)
- 镜像每日自动同步，可能存在延迟
- 请确保主机目录 `/home/ubuntu/data/new-api` 存在且有适当权限
- 每次同步会创建一个新的带时间戳的版本标签，确保可以追踪每次同步

## 📊 统计信息

- **最后同步时间**: 2025-11-01 06:36:39 +0000 UTC
- **同步触发方式**: 手动触发
- **同步状态**: 成功
- **当前版本**: 20251101081118

---

*此 README 由 GitHub Actions 自动更新*
