# 📦 发布指南

**创建时间**：2026-03-19  
**版本**：v1.0  
**维护人**：主助手（总指挥）

---

## 发布到 GitHub

### 步骤 1：初始化 Git 仓库

```bash
cd /Users/laihehuo/.openclaw/workspace-main/agents/main/skills/task-decomposition/
git init
git add .
git commit -m "Initial commit: task-decomposition skill v1.0"
```

### 步骤 2：创建 GitHub 仓库

1. 登录 GitHub：https://github.com
2. 创建新仓库：`task-decomposition`
3. 设置为公开仓库（Public）
4. 添加 README.md、LICENSE、.gitignore

### 步骤 3：关联远程仓库

```bash
git remote add origin https://github.com/jiebao360/task-decomposition.git
git branch -M main
git push -u origin main
```

### 步骤 4：验证发布

访问：https://github.com/jiebao360/task-decomposition

确认文件结构：
```
task-decomposition/
├── SKILL.md
├── README.md
├── LICENSE
├── PUBLISH.md
├── clawhub.json
├── config/
│   └── lobster-team.md
├── templates/
│   └── task-templates.md
└── docs/
    ├── auto-create-feishu-doc.md
    └── task-tracking.md
```

---

## 发布到 Clawhub

### 步骤 1：配置 Clawhub

确保已安装 Clawhub CLI：
```bash
npm install -g clawhub
```

### 步骤 2：登录 Clawhub

```bash
clawhub login
```

### 步骤 3：验证配置

```bash
clawhub validate
```

### 步骤 4：发布技能

```bash
clawhub publish
```

### 步骤 5：验证发布

访问：https://clawhub.ai/skills/task-decomposition

---

## 版本更新

### 更新版本号

编辑 `clawhub.json`：
```json
{
  "version": "1.0.1"  // 更新版本号
}
```

### 提交更新

```bash
git add .
git commit -m "Update to v1.0.1: [更新说明]"
git push
```

### 发布新版本

```bash
clawhub publish
```

### 创建 Git Tag

```bash
git tag v1.0.1
git push origin v1.0.1
```

---

## 维护指南

### 添加新功能

1. 在 `SKILL.md` 中添加新功能说明
2. 在 `templates/` 中添加新模板
3. 在 `docs/` 中添加新文档
4. 更新 `README.md`
5. 更新版本号
6. 提交并发布

### 修复 Bug

1. 修复问题
2. 在 `SKILL.md` 中记录修复
3. 更新版本号（补丁版本，如 1.0.1 → 1.0.2）
4. 提交并发布

### 重大更新

1. 更新主要功能
2. 在 `SKILL.md` 中记录变更
3. 更新版本号（主要版本，如 1.0.0 → 2.0.0）
4. 在 `README.md` 中记录不兼容变更
5. 提交并发布

---

## 推广技能

### 1. 在 OpenClaw 社区推广

- 在 OpenClaw 论坛发布技能介绍
- 在 Discord 社区分享
- 在微信群/QQ 群分享

### 2. 编写使用教程

- 编写详细使用教程
- 录制视频教程
- 分享成功案例

### 3. 收集反馈

- 在 GitHub Issues 收集反馈
- 在 Clawhub 页面收集评价
- 持续改进技能

---

## 常见问题

### Q1：发布失败怎么办？

A：检查以下几点：
1. Git 仓库是否正确初始化
2. clawhub.json 配置是否正确
3. 是否已登录 Clawhub
4. 网络连接是否正常

### Q2：如何更新已发布的技能？

A：
1. 更新本地文件
2. 更新版本号
3. 提交到 Git
4. 运行 `clawhub publish`

### Q3：如何删除已发布的技能？

A：
1. 在 Clawhub 页面找到技能
2. 点击"Delete"删除
3. 在 GitHub 删除仓库（可选）

### Q4：如何添加合作维护者？

A：
1. 在 GitHub 仓库添加 Collaborator
2. 在 Clawhub 添加维护者权限
3. 在 `SKILL.md` 中更新维护人信息

---

## 相关资源

- [Clawhub 文档](https://clawhub.ai/docs)
- [OpenClaw 文档](https://docs.openclaw.ai)
- [GitHub 文档](https://docs.github.com)

---

*指南创建时间：2026-03-19*  
*指南版本：v1.0*  
*维护人：主助手（总指挥）*
