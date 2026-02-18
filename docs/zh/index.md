<p align="center">
  <img src="../assets/logo.svg" alt="DblpService Logo" width="56" style="vertical-align:middle;" />
  <span style="font-size:1.8rem;font-weight:700;vertical-align:middle;margin-left:8px;">DblpService 文档</span>
</p>

DblpService 是 CoAuthors 与 CiteVerifier 共同使用的 DBLP 构建与查询后端。

## 核心职责

- DBLP 源数据下载与本地构建流水线
- Bootstrap 控制台（`/bootstrap`）
- 健康检查、统计与共作查询接口
- Pipeline 生命周期控制（`start / stop / reset / state`）

## 集成范围

- 默认服务端口：`8091`
- 作为 `CoAuthors` 的直接后端
- 作为 `CiteVerifier` 的共享/备用构建查询后端

## 运行特性

- 基于 SQLite 的查询服务（`dblp.sqlite`）
- 查询接口执行前进行 fullmeta schema 校验
- 可配置数据库锁等待超时（`DB_BUSY_TIMEOUT_MS`）
- 通过 `CORS_ORIGINS` 管理跨域访问

## 推荐阅读顺序

1. [快速开始](quickstart.md)
2. [配置说明](configuration.md)
3. [接口说明](api.md)
4. [开发文档](develop.md)
5. [运维手册](operations.md)
6. [故障排查](troubleshooting.md)
7. [变更记录](changelog.md)
