# GitHub 仓库信息

## 仓库信息

- **仓库地址：** https://github.com/Zixi370719/Data-Standardization.git
- **所有者：** Zixi370719
- **仓库名：** Data-Standardization

## Personal Access Token

**警告：** 不要将token提交到公开仓库。请联系管理员获取token。

## 推送方式

### 方法1：GitHub API（推荐）

使用curl命令直接调用GitHub API：

```bash
# 文件内容base64编码
base64 -w 0 your_file.md > /tmp/file_base64.txt

# 创建/更新文件
curl -X PUT \
  'https://api.github.com/repos/Zixi370719/Data-Standardization/contents/your_file.md' \
  -H 'Authorization: token YOUR_TOKEN_HERE' \
  -H 'Content-Type: application/json' \
  -d '{
    "message": "Commit message here",
    "content": "'"$(cat /tmp/file_base64.txt)"'"
  }'
```

### 方法2：Git命令

配置remote URL并push：

```bash
cd /home/node/.openclaw/workspace
git remote set-url origin https://YOUR_TOKEN@github.com/Zixi370719/Data-Standardization.git
git push origin master
```

### 方法3：SSH（如果已配置）

```bash
git remote set-url origin git@github.com:Zixi370719/Data-Standardization.git
git push origin master
```

## 近期推送记录

| 日期 | 文件 | Commit SHA | 备注 |
|------|------|-----------|------|
| 2026-04-02 | 2026Q1数据标准化工作进展报告-高可信度版.md | da02b000 | GitHub API推送成功 |
| 2026-04-02 | PUSH_INSTRUCTIONS.md | 55954e83 | GitHub API推送成功 |

---

**创建时间：** 2026-04-02
**最后更新：** 2026-04-02
