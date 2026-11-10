# Marco TV

免费开源的 Android 电视桌面，源码位于 [`MarcoTV/`](MarcoTV/)。

## 云构建

推送代码后由 GitHub Actions 自动构建（`.github/workflows/marco-build.yml`，Windows runner）：

1. `python scripts/bootstrap.py` 拉取官方 Android 工具链
2. `python scripts/build.py` 编译并签名
3. 产物 `MarcoTV/dist/MarcoTV-*.apk` 上传为 artifact

也可在 Actions 页面手动触发（workflow_dispatch）。

## 本地构建

```sh
cd MarcoTV
python scripts/bootstrap.py
python scripts/build.py
```

产物在 `MarcoTV/dist/`。