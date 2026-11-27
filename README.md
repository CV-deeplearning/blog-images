# blog-images

这是公开博客图床仓库，用来托管 CSDN、微信公众号和知乎文章中的配图。

## CDN 访问地址

把图片推到本仓库的 `main` 分支后，用 jsDelivr 访问：

```
https://cdn.jsdelivr.net/gh/CV-deeplearning/blog-images@main/<路径>
```

例如：

```
https://cdn.jsdelivr.net/gh/CV-deeplearning/blog-images@main/csdn/CodexGuide/cover.png
```

若 jsDelivr 尚未刷新，可用 GitHub 原始地址作为备用：

```
https://raw.githubusercontent.com/CV-deeplearning/blog-images/main/<路径>
```

## 目录约定

- `csdn/<文章名>/`：对应一篇 CSDN 文章的全部配图
