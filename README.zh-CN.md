<p align="center">
  <img src="./static/dblpservice-logo.svg" alt="DblpService Logo" width="52" />
  <strong>DblpService</strong>
</p>

<p align="center">DBLP 鏁版嵁鏋勫缓涓庢煡璇㈠悗绔湇鍔°€?/p>

<p align="center">
  <a href="./README.md"><strong>EN</strong></a> |
  <a href="./README.zh-CN.md"><strong>CN</strong></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-0.1.0-1f7a8c" alt="version" />
  <img src="https://img.shields.io/badge/python-3.10%2B-3776AB?logo=python&logoColor=white" alt="python" />
  <img src="https://img.shields.io/badge/FastAPI-0.111%2B-009688?logo=fastapi&logoColor=white" alt="fastapi" />
  <img src="https://img.shields.io/badge/docs-MkDocs-526CFE?logo=materialformkdocs&logoColor=white" alt="docs" />
</p>

## 椤圭洰璇存槑

DblpService 鏄彲澶嶇敤鐨?DBLP 鍚庣锛岃礋璐ｆ暟鎹笅杞姐€佽В鏋愩€丼QLite 寤哄簱鍜屾煡璇㈡湇鍔°€?瀹冨彲浠ヨ CoAuthors銆丆iteVerifier 浠ュ強鍏朵粬闇€瑕佹湰鍦?DBLP 鏁版嵁鑳藉姏鐨勭郴缁熷鐢ㄣ€?
## 鏍稿績鑳藉姏

- DBLP 婧愭暟鎹笅杞戒笌瑙ｆ瀽娴佹按绾?- Bootstrap 绠＄悊椤甸潰锛坄/bootstrap`锛?- 鏌ヨ鎺ュ彛锛坄/api/health`銆乣/api/stats`銆乣/api/coauthors/pairs`锛?- Pipeline 鎺у埗鎺ュ彛锛坄/api/start`銆乣/api/stop`銆乣/api/reset`銆乣/api/state`锛?
## 蹇€熷紑濮?
```bash
cd DblpService
python -m pip install -r requirements.txt
python -m uvicorn app:app --host 0.0.0.0 --port 8091
```

璁块棶锛?
- `http://localhost:8091/bootstrap`
- `http://localhost:8091/`

## 鍏抽敭鐜鍙橀噺

- `DATA_DIR`锛堥粯璁わ細`./data`锛?- `DB_PATH`锛堥粯璁わ細`${DATA_DIR}/dblp.sqlite`锛?- `CORS_ORIGINS`锛堥€楀彿鍒嗛殧锛?- `DB_BUSY_TIMEOUT_MS`锛堥粯璁わ細`30000`锛?
## 鏂囨。

- 鑻辨枃鏂囨。锛歚docs/en/`
- 涓枃鏂囨。锛歚docs/zh/`

鏈湴棰勮锛?
```bash
cd DblpService
python -m pip install -r docs/requirements.txt
mkdocs serve
```
