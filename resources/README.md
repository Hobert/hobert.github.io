# 开源资料使用说明

## 📁 文件夹结构

```
个人主页/
├── open-resources.json    # 资料配置文件
└── resources/              # 资料存放文件夹
    └── [您的资料文件]
```

## 🚀 如何添加新资料

### 步骤1：准备资料文件
将您的资料文件（PDF、ZIP等）放入 `resources/` 文件夹中。

### 步骤2：编辑配置文件
打开 `open-resources.json` 文件，在数组中添加新的资料对象：

```json
{
  "id": "5",
  "title": "资料标题",
  "description": "资料详细描述",
  "category": "竞赛资料",
  "tags": ["标签1", "标签2", "标签3"],
  "fileUrl": "https://github.com/hobert/akebi.github.io/raw/main/resources/文件名.zip",
  "fileSize": "10.5 MB",
  "uploadDate": "2026-03-08",
  "downloads": 0
}
```

### 字段说明：
- `id`: 唯一标识符（数字即可）
- `title`: 资料标题
- `description`: 资料详细描述
- `category`: 分类（可选：竞赛资料、代码库、学习资料、开发模板）
- `tags`: 标签数组
- `fileUrl`: 下载链接（GitHub raw链接）
- `fileSize`: 文件大小
- `uploadDate`: 上传日期
- `downloads`: 下载次数

### 步骤3：获取GitHub Raw链接
1. 将资料文件上传到GitHub仓库的 `resources/` 文件夹
2. 在GitHub上打开该文件
3. 点击 "Raw" 按钮
4. 复制浏览器地址栏的URL作为 `fileUrl`

### 步骤4：提交并推送
```bash
git add open-resources.json resources/
git commit -m "添加新资料：[资料名称]"
git push
```

## 📋 分类说明

- **竞赛资料**: 各类竞赛相关资料
- **代码库**: 可复用的代码项目
- **学习资料**: 课程笔记、学习指南等
- **开发模板**: 项目模板、脚手架等

## 💡 小贴士

1. 文件大小建议控制在50MB以内
2. 使用清晰的文件名，便于识别
3. 标签有助于用户快速找到资料
4. 定期更新下载次数统计
