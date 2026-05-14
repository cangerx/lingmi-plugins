# 灵觅AI 插件市场

这是灵觅AI的官方插件仓库。开发者可以提交插件到这里，所有灵觅AI用户都可以在管理后台一键安装。

## 提交插件

1. Fork 本仓库
2. 在 `plugins/your-plugin/` 下放置 `plugin.yaml`
3. 创建 GitHub Release，上传 `your-plugin.tar.gz`
4. 在 `registry.json` 中添加你的插件条目
5. 提交 Pull Request

## registry.json 格式

```json
{
  "plugins": [
    {
      "slug": "your-plugin",
      "name": "插件名称",
      "description": "插件描述",
      "version": "1.0.0",
      "author": "作者",
      "icon": "图标URL",
      "download_url": "https://github.com/cangerx/lingmi-plugins/releases/download/your-plugin-v1.0.0/your-plugin.tar.gz",
      "min_version": "1.0.0",
      "tags": ["标签1", "标签2"],
      "size": "1.2MB"
    }
  ]
}
```

## 插件打包

```bash
# 目录结构
your-plugin/
├── plugin.yaml
├── web/dist/        # 前端构建产物
└── server/          # 后端代码（可选）

# 打包
tar -czf your-plugin.tar.gz your-plugin/
```

## 开发文档

完整开发指南请参考：[插件开发文档](https://github.com/cangerx/lingmi-ai/blob/main/docs/plugin-guide.md)
