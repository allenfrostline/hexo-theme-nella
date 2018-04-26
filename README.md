This Theme is forked from https://github.com/pinggod/hexo-theme-apollo   

Original document in [English](https://github.com/pinggod/hexo-theme-apollo/blob/master/doc%2Fdoc-en.md) | [中文](https://github.com/pinggod/hexo-theme-apollo/blob/master/doc/doc-zh.md)

### Changes in this version:
1. add tag and category support with UI
2. add site content search (posts + pages)
3. Change container width from `700px` to `800px`, to support more tabs in navigation

Checkout the live demo: https://hzhou.me

### Installation
``` bash
# Quick basic installation
cd ${hexo-blog-folder}
npm install --save hexo-renderer-jade hexo-generator-feed hexo-generator-sitemap hexo-browsersync hexo-generator-archive
git clone https://github.com/zhouhao/hexo-theme-apollo-plus.git themes/apollo
```
Modify `_config.yml` for your blog

```yaml
theme: apollo

# display all blogs in a list in archive page
# plugin hexo-generator-archive is required
archive_generator:
    per_page: 0
    yearly: false
    monthly: false
    daily: false
```

### Enable category and tag entry page
> demo: https://hzhou.me/tags/

To have this page, you have to create a new page named `tags`
```bash
hexo new page tags
# you can change the `title`, otherwise its default value is "tags"
```
Add its tab in navigation menu in theme `_config.yml` file
```
# https://github.com/zhouhao/hexo-theme-apollo-plus/blob/master/_config.yml#L4
menu:
    # ...
    Tag: /tags/
    # ...
```

### Enable site search
**NOTE**: `search` entry is added in [layout/partial/nav.jade](https://github.com/zhouhao/hexo-theme-apollo-plus/blob/master/layout/partial/nav.jade#L12), if you want to disable `site search`, just remove this line

> demo: https://hzhou.me/search/

```bash
npm install hexo-generator-tipue-search-json --save
hexo new page search # also you can change its `title` in search/index.md file
```

Then modify `search/index.md` as below:(change `title` and `date` as whatever you like)
```md
title: Site Search
date: 2017-04-30 16:58:14
---

<form id="search-form" style="text-align:center;">
  <i class="fa fa-search tipue_search_icon"></i>
  <input  type="text" name="q" id="tipue_search_input" autocomplete="off" required placeholder="Type, Enter and Search" />
</form>

<div id="tipue_search_content"></div>
```    
### All Set now!!!

### License

MIT
