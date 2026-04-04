# OpenAI-New API 镜像同步仓库

## 📋 项目简介

本仓库自动同步 [calciumion/new-api](https://hub.docker.com/r/calciumion/new-api) Docker 镜像到 GitHub Container Registry (GHCR)。

## 🚀 镜像信息

- **镜像地址**: `ghcr.io/bqizkm01918t/openai-new:latest`
- **镜像大小**: 162MB
- **源镜像**: `calciumion/new-api:latest`
- **同步频率**: 每日自动同步 (北京时间上午 10 点)
- **当前版本**: v12
- **版本策略**: 循环使用 v0-v19 共20个标签

## 📅 最近同步记录 (最新10条)

| 同步时间 | 版本标签 | 触发方式 | 状态 |
|----------|----------|----------|------|
| 2026-04-04 04:08:14 | v12 | 自动执行 | ✅ |
| 2026-04-03 04:22:14 | v11 | 自动执行 | ✅ |
| 2026-04-02 04:21:21 | v10 | 自动执行 | ✅ |
| 2026-04-01 04:40:27 | v9 | 自动执行 | ✅ |
| 2026-03-31 04:28:46 | v8 | 自动执行 | ✅ |
| 2026-03-30 04:37:34 | v7 | 自动执行 | ✅ |
| 2026-03-29 04:29:38 | v6 | 自动执行 | ✅ |
| 2026-03-28 04:10:45 | v5 | 自动执行 | ✅ |
| 2026-03-27 04:26:24 | v4 | 自动执行 | ✅ |
| 2026-03-26 04:24:57 | v3 | 自动执行 | ✅ |

## 🏷️ 可用版本标签

- **最新版本**: `latest` (始终指向最新版本)
- **历史版本**: v0, v1, v10, v11, v12, v13, v14, v15, v16, v17, v18, v19, v2, v3, v4, v5, v6, v7, v8, v9

> ⚠️ 注意：系统自动循环使用 v0-v19 共20个标签，旧版本会被新版本覆盖。

## 🔄 版本管理策略

1. 使用 **循环标签系统** (v0 → v19 → v0)
2. 自动覆盖最老的标签
3. 始终保留最近20个版本
4. `latest` 标签始终指向最新版本

## 📦 使用方法

### 使用最新版本

```bash
# 使用latest标签（推荐）
docker run --name new-api -d --restart always \
  -p 3000:3000 \
  -e TZ=Asia/Shanghai \
  -v /home/ubuntu/data/new-api:/data \
  ghcr.io/bqizkm01918t/openai-new:latest
```

### 使用特定版本

```bash
# 使用特定版本标签
docker run --name new-api -d --restart always \
  -p 3000:3000 \
  -e TZ=Asia/Shanghai \
  -v /home/ubuntu/data/new-api:/data \
  ghcr.io/bqizkm01918t/openai-new:v12
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

## 📊 统计信息

- **最后同步时间**: 2026-04-04 04:08:19 UTC
- **当前版本标签**: v12
- **同步触发方式**: 自动执行
- **同步状态**: ✅ 成功

## ⚠️ 注意事项

- 本镜像仅作同步用途，请勿用于生产环境
- 版本标签循环使用，超过20个版本后会覆盖旧版本
- 如需长期保存特定版本，请自行备份
- 镜像每日自动同步，可能存在延迟

---

*此 README 由 GitHub Actions 自动更新于 2026-04-04 04:08:19 UTC*
