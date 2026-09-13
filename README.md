# 奇点异客工作室 · 百科网页

纯静态站点，双击 `index.html` 就能在浏览器里预览，不需要安装任何环境。

## 目录结构

```
singularity-wiki/
├── index.html        首页（上方简介板块 + 下方四个卡片入口）
├── members.html      成员信息页（内容待补充）
├── works.html        作品页（内容待补充）
├── page-3.html       板块三：空白页，主题待定
├── page-4.html       板块四：空白页，主题待定
├── members/          成员个人简介页
│   ├── jiang-yunting.html    江韵婷（主席）
│   ├── zhou-pengcheng.html   周鹏程（副主席）
│   ├── zhang-junru.html      张钧儒（负责人）
│   └── huang-zhi.html        黄智（负责人）
├── image/            素材目录：放待替换的图片和视频（见 image/README.md）
│   ├── logo/         正式 logo
│   ├── members/      成员照片
│   ├── works/        作品封面与截图
│   └── video/        宣传片、演示视频
└── assets/
    ├── css/style.css 全站样式
    └── img/
        ├── logo.svg          占位 logo
        └── members/          成员照片目录（含保底占位图 placeholder.svg）
```

## 接下来怎么改

- **换 logo**：直接用正式图片覆盖 `assets/img/logo.svg`（如果换成 png/jpg，记得把页面里 `logo.svg` 的引用一起改掉）。
- **改简介**：`index.html` 中搜索 `hero__intro`，替换那一段占位文字。
- **换成员照片**：把照片放进 `assets/img/members/`，建议 1:1 正方形、边长 400px 以上，文件名用拼音（如 `jiang-yunting.jpg`）；
  然后在 `members.html` 里把对应用户那张卡片的 `src="assets/img/members/placeholder.svg"` 改成新文件名，`alt` 也顺手改一下。
- **写成员简介**：`members.html` 里每个成员卡片下方都有 `member__bio` 那一段，替换掉「简介待补充……」即可。
- **改个人简介页**：`members/` 下已建好主席与负责人的四张个人页，每页分「个人简介 / 职责 / 参与作品与经历」三块，右侧是基本信息栏，
  `待补充` 三处分别对应加入时间、负责方向。新增成员个人页时，复制任意一个已有页面改名最快，注意页面里的相对路径是 `../`（因为文件在子目录里）。
- **定板块三 / 四**：先把 `index.html` 里两张 `card--todo` 卡片的标题、简介和链接改掉，再改对应页面里的标题和内容；如果要换文件名，两个地方都要同步。
- **改配色**：`assets/css/style.css` 顶部的 `:root` 变量里改 `--accent` 就能整体换主色。
- **页脚年份**：各页面底部的 `© 2026` 按需修改。
