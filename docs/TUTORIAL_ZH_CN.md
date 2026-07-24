# Megalo Image Generator Pro v1.43 新手教程

## 下载与安装

从Releases下载 `Megalo_Pro_v1.43_GitHub_Free_protected_20260724.zip`。GitHub自动生成的源代码ZIP不是安装包。

解压后，在 `chrome://extensions` 中启用开发者模式并加载 `zh_CN/extension`。

## 更新Cloud Run后端

v1.43加入了新的Gemini模型，因此从v1.42升级时必须使用附带的v1.43脚本重新部署Cloud Run后端。

## v1.43模型

- 默认图像：`gemini-3.1-flash-image`
- 高质量图像：`gemini-3-pro-image`
- 低成本1K图像：`gemini-3.1-flash-lite-image`
- 默认文本：`gemini-3.6-flash`
- 轻量文本备用：`gemini-3.5-flash-lite`

已停止的Preview模型已被移除，旧选择会自动迁移。Flash Lite Image仅支持1K。

## 恢复旧配置

导入旧预设、角色文件、文件夹备份或加密备份时，当前Backend URL槽位1至10不会被覆盖。
