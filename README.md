# Luo9 插件注册表

此仓库存储 Luo9 Bot 的插件注册信息，供 `luo9` CLI 工具使用。

## 插件列表

| 插件 | 说明 | 最新版本 |
|------|------|----------|
| ai_chat | AI 对话插件 | 3.1.0 |
| epic | Epic Games 免费游戏查询 | 0.2.2 |
| doro | Doro 每日结局 | 0.1.1 |

## 插件发布

插件通过 GitHub Actions 自动向此仓库提交 PR，管理员审核后合并即生效。

## 注册表格式

```json
{
  "plugins": {
    "<crate_name>": {
      "description": "插件说明",
      "repo": "luo9-bot/<repo_name>",
      "config_files": [],
      "versions": [
        {
          "version": "1.0.0",
          "tag": "v1.0.0",
          "sdk_version": "0.5.2",
          "assets": {
            "windows-x86_64": "lib<crate_name>.dll",
            "linux-x86_64": "lib<crate_name>.so"
          }
        }
      ]
    }
  }
}
```
