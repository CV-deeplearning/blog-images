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

## 如何上传

推荐在已登录 `gh` 的机器上，运行配套脚本 `upload_images.sh`，它会把 `images/` 里的 PNG 上传到 `csdn/<文章名>/`，并生成把相对路径换成 CDN 链接的 `article-cdn.md`。

仓库里还保留了一个需手动触发的工作流 `.github/workflows/decode-images.yml`：把 `staging/<目标路径>.b64`（标准 base64 文本）推到 `main` 后，在 Actions 里运行 “Decode staged images”，它会解码成 PNG、提交到对应路径，并删掉暂存文件。首次搭建时接口不能直接写二进制文件，就是走的这条路径。
