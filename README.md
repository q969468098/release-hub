# Release Hub

应用发布中枢。每个子目录对应一个应用，包含版本检测 JSON 文件。

```
release-hub/
├── api-key-checker/
│   └── latest.json       ← 版本检测端点
├── downloads/            ← 安装包 (.msi / .sig)
├── publish.bat           ← 一键发布脚本（从项目目录运行）
└── README.md
```

## 版本检测地址

```
https://q969468098.github.io/release-hub/api-key-checker/latest.json
```

## 发布新版本

在对应项目目录下运行 `publish.bat`，自动完成：
1. 读取版本号
2. 复制 .msi + .sig 到 downloads/
3. 更新 latest.json
4. 提交并推送到 GitHub

## 新增应用

```bash
mkdir 新应用名
# 创建 latest.json 模板
```
