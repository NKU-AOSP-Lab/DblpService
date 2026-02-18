<p align="center">
  <img src="./static/dblpservice-logo.svg" alt="DblpService Logo" width="56" style="vertical-align:middle;" />
  <span style="font-size:2rem;font-weight:700;vertical-align:middle;margin-left:10px;">DblpService</span>
</p>

<p align="center">DBLP build-and-query backend service for CoAuthors and CiteVerifier.</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-0.1.0-1f7a8c" alt="version" />
  <img src="https://img.shields.io/badge/python-3.10%2B-3776AB?logo=python&logoColor=white" alt="python" />
  <img src="https://img.shields.io/badge/FastAPI-0.111%2B-009688?logo=fastapi&logoColor=white" alt="fastapi" />
  <img src="https://img.shields.io/badge/docs-MkDocs-526CFE?logo=materialformkdocs&logoColor=white" alt="docs" />
</p>

## 中文说明

DblpService 负责 DBLP 数据下载、解析、建库与查询服务，是 CoAuthors / CiteVerifier 的后端基础能力。

### 核心能力

- Bootstrap 管理页面（`/bootstrap`）
- DBLP 查询接口（健康、统计、共作查询）
- Pipeline 控制接口（开始、停止、重置、状态）
- 本地 SQLite 数据服务（`dblp.sqlite`）

### 本地启动

```bash
cd DblpService
python -m pip install -r requirements.txt
set CORS_ORIGINS=http://localhost:8090
python -m uvicorn app:app --host 0.0.0.0 --port 8091
```

访问：

- `http://localhost:8091/bootstrap`
- `http://localhost:8091/`

### 关键环境变量

- `DATA_DIR`（默认 `./data`）
- `DB_PATH`（默认 `${DATA_DIR}/dblp.sqlite`）
- `CORS_ORIGINS`（逗号分隔）
- `DB_BUSY_TIMEOUT_MS`（默认 `30000`）

### 文档

- 中文：`docs/zh/`
- English：`docs/en/`
- 本地预览：

```bash
cd DblpService
python -m pip install -r docs/requirements.txt
mkdocs serve
```

## English Overview

DblpService is the DBLP backend that handles data bootstrap, SQLite build, and query APIs.

### Capabilities

- Bootstrap web console
- Health/stats/query APIs
- Pipeline lifecycle control
- Fullmeta-compatible SQLite serving

### Run Locally

```bash
cd DblpService
python -m pip install -r requirements.txt
python -m uvicorn app:app --host 0.0.0.0 --port 8091
```

### Documentation

- Chinese docs: `docs/zh/`
- English docs: `docs/en/`
