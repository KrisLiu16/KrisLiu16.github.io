# 个人主页（GitHub Pages）

单文件静态页面 `index.html`，学术风格（左栏姓名、头衔与外链，右栏简介、工作经历、教育经历），无外部依赖，手机宽度下改为单栏。

`demos/` 目录里是选型时的三个 demo，正式页面不引用它们。

## 修改内容

打开 `index.html`，改这几处：

- `<title>`、左栏 `<h1>`、`.sub`：名字、英文名、头衔
- 左栏 `<ul>`：LinkedIn、GitHub 链接
- `简介`：个人简介段落
- `工作经历`、`教育经历`：每段是一个 `<div class="entry">`，`.head` 为职位与公司，`.when` 为时间地点

## 部署到 GitHub Pages

用户主页地址是 `https://<用户名>.github.io`，需要一个名为 `<用户名>.github.io` 的仓库，内容放在默认分支根目录。

```bash
cd /home/ubuntu/workspace/homepage
git init -b main
git add index.html README.md
git commit -m "Add personal homepage"
git remote add origin https://github.com/KrisLiu16/KrisLiu16.github.io.git
git push -u origin main
```

推送后到仓库 **Settings → Pages**，Source 选 `Deploy from a branch`，Branch 选 `main` / `/ (root)`，保存。约一分钟后访问 `https://krisliu16.github.io`。

注意：仓库需先在 GitHub 上创建（名字必须是 `KrisLiu16.github.io`，且为 public，除非账号是付费计划）。提交前确认 git 用户信息是你要的身份。
