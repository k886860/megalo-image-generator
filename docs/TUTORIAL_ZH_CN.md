# Megalo Image Generator Pro v1.42 新手教程

本教程面向首次使用Chrome扩展程序、Google Cloud和Vertex AI的用户。

## 1. 使用前须知

程序本身免费，但图像和视频生成通过用户自己的Google Cloud项目执行，因此可能产生Vertex AI和Cloud Run费用。

首次测试请只使用一张参考图、一个场景、一张输出以及1K或2K分辨率。

## 2. 下载与安装

从本仓库的 **Releases** 页面下载 `Megalo_Pro_v1.42_GitHub_Free_protected_20260716.zip`。GitHub自动生成的 `Source code (zip)` 不是应用程序安装包。

完整解压ZIP后：

1. 在Chrome中打开 `chrome://extensions`。
2. 启用**开发者模式**。
3. 点击**加载已解压的扩展程序**。
4. 选择 `zh_CN/extension`。

## 3. 准备Google Cloud

需要已连接结算账号并拥有Vertex AI访问权限的Google Cloud项目。程序中应填写 **Project ID**，而不是项目显示名称。

![查找Project ID](assets/gcp_01_project_id.png)

部署可能需要启用Vertex AI、Cloud Run Admin、Cloud Build、Artifact Registry和Service Usage API。

## 4. 部署Cloud Run后端

1. 打开 `SCENE` 场景生成标签页。
2. 展开 `Vertex / 后端设置`中的槽位1。
3. 输入别名与Project ID。
4. 创建并复制自动重新部署脚本。
5. 在Google Cloud Shell中运行该脚本。

![运行部署命令](assets/gcp_04_deploy_commands.png)

部署结束后，复制以 `https://` 开头的Cloud Run服务URL，并粘贴到同一槽位的Backend URL中。

![Cloud Run URL](assets/gcp_05_service_url.png)

## 5. 参考图

| 槽位 | 默认作用 |
|---|---|
| 1 | 面部与发型身份 |
| 2 | 全身正面与服装正面 |
| 3 | 侧面轮廓与侧面剪影 |
| 4 | 全身背面与背部细节 |
| 5 | 面部与服装补强 |

五张图并非全部必需。连接测试时只使用一张面部参考图即可。生成前请确认预览区显示的是实际图像。

## 6. 生成第一张图像

系统提示词示例：

```text
一名成年角色。保持与上传参考图相同的面部和发型。
现代高分辨率真人摄影。画面中无文字、标志或水印。
```

场景提示词示例：

```text
[场景] 成年角色在明亮的室内摄影棚中自然站立并看向镜头。自然的全身构图和柔和灯光。
```

选择画面比例、1K或2K分辨率、输出一张图像，检查最终提示词后开始自动生成。生成进行时不要反复点击按钮。

## 7. 查看与保存

在 `SAVE` 标签页中可以查看、排序、重新生成、删除和保存结果。分屏图像可使用自动分割或手动分割工具。

## 8. 费用与恢复

批量生成前，请设置槽位余额和生成安全中心，包括批次预算、会话预算与紧急备份。

Chrome异常退出后，在清除浏览器数据之前先查看崩溃恢复和生成历史。

## 9. 常见错误

- **403：**检查Vertex AI API、模型访问权限、Project ID及Cloud Run服务账号权限。
- **429：**减少并发槽位、重试次数和批次大小，等待一段时间后再试。
- **Failed to fetch：**检查Backend URL与Cloud Run服务运行状态。
- **参考图还原度低：**删除互相冲突的描述，减少参考图数量并简化场景。
- **内存不足：**关闭无关标签页，将任务拆成小批次，保存后重新启动Chrome。

## 10. 更新

将新Release解压到新的文件夹。切换扩展程序目录前，请备份预设、角色、参考图集和生成结果。
