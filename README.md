# OpenAI-New API 镜像同步仓库

## 📋 项目简介

本仓库自动同步 [calciumion/new-api](https://hub.docker.com/r/calciumion/new-api) Docker 镜像到 GitHub Container Registry (GHCR)。

## 🚀 镜像信息

- **镜像地址**: `ghcr.io/bqizkm01918t/openai-new:latest`
- **镜像大小**: 68.4MB
- **源镜像**: `calciumion/new-api:latest`
- **同步频率**: 每日自动同步 (北京时间上午 10 点)

## 📅 同步记录

| 同步时间 | 触发方式 | 状态 |
|----------|----------|------|
| 2025-11-01 07:57:43 UTC | 手动触发 | ✅ 成功 |

## 🔄 同步流程

1. 从 Docker Hub 拉取最新 `calciumion/new-api` 镜像
2. 重新标记为 `ghcr.io/bqizkm01918t/openai-new`
3. 推送到 GitHub Container Registry
4. 更新本 README 文件

## 📦 使用方法

### Docker 命令

```bash
docker pull ghcr.io/bqizkm01918t/openai-new:latest
docker run -d --name openai-new -p 3000:3000 ghcr.io/bqizkm01918t/openai-new:latest
```

### Docker Compose

```yaml
version: '3'
services:
  openai-new:
    image: ghcr.io/bqizkm01918t/openai-new:latest
    container_name: openai-new
    ports:
      - "3000:3000"
    restart: unless-stopped
```

## ⚠️ 注意事项

- 本镜像仅作同步用途，请勿用于生产环境
- 如需了解原始项目详情，请访问 [calciumion/new-api](https://hub.docker.com/r/calciumion/new-api)
- 镜像每日自动同步，可能存在延迟

## 📊 统计信息

- **最后同步时间**: 2025-11-01 06:36:39 +0000 UTC
- **同步触发方式**: 手动触发
- **同步状态**: 成功

---

*此 README 由 GitHub Actions 自动更新*
