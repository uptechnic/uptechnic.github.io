# 介绍

王传军的技术博客，学习，分享，成长。

# 本地运行

一般提交到 github 过个几十秒就可以看到效果，如果你需要对在本地查看效果需要安装 ruby 环境和依赖

windows 下推荐在 wsl 下装 ruby，直接一句`apt install build-essential ruby ruby-dev` 就行了

```bash
# linux下需要gcc

# gem sources --add https://gems.ruby-china.com/
# gem sources --remove https://rubygems.org/
# gem sources --remove https://mirrors.aliyun.com/rubygems/
# gem sources -l
gem install bundler
# bundle config mirror.https://rubygems.org https://gems.ruby-china.com
bundle install
```

通过下面命令启动/编译项目

```bash
bundle exec jekyll serve --watch --host=127.0.0.1 --port=8080
bundle exec jekyll build --destination=dist
```

如果需要替换代码高亮的样式可以通过下面的命令生成 css

```bash
rougify help style
rougify style github > highlighting.css
```

# 项目配置

1. 修改`pages/about.md`中关于我的内容

2. 修改`_config.yml`文件，具体作用请参考注释

3. 清空`post _posts`目录下所有文件，注意是清空，不是删除这两个目录

4. 网站的 logo 和 favicon 放在了`static/img/`下，替换即可，大小无所谓，图片比例最好是 1:1

5. 如果你是把项目 fork 过去的，想要删除我的提交记录可以先软重置到第一个提交，然后再提交一次，最后强制推送一次就行了

# 使用

文章放在`_posts`目录下，命名为`yyyy-MM-dd-xxxx-xxxx.md`，内容格式如下

```yaml
---
layout: post
title: 标题
categories: [分类1, 分类2]
extMath: true # 是否启用数学公式支持
toc: true # 是否自动生成目录
---
文章内容，Markdown格式
```

文章资源放在`posts`目录，如文章文件名是`2019-05-01-theme-usage.md`，则该篇文章的资源需要放在`posts/2019/05/01`下,在文章使用时直接引用即可。当然了，写作的时候会提示资源不存在忽略即可

```md
![这是图片](xxx.png)

[xxx.zip 下载](xxx.zip)
```
