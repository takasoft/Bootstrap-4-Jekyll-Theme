# Bootstrap 4 Jekyll Theme

Simple Bootstrap 4 theme for Jekyll

## Features 

✓ Command-line workflow, using GitHub.com to create, customize and post to your blog  <br>
✓ Fully responsive and mobile optimized base theme ([Demo](https://takao42.github.io/Bootstrap-4-Jekyll-Theme/))  <br>
✓ Free hosting on your GitHub Pages user site  <br>
✓ Very light weight. It loads very fast even in 2G connections.  <br>
✓ Markdown blogging  <br>

✘ No installing dependencies  <br>
✘ No need to set up local development  <br>
✘ No configuring plugins  <br>
✘ No need to spend time on theming  <br>

## Quick start

### Step 1) Fork this theme to your user repository

Fork this repository, then rename the repository to your-username.github.io or your favorite name.

### Step 2) Enable Github Pages

Go to `Settings --> Github Pages --> Source`

Choose `master branch` and enable Github Pages.

Your Jekyll blog will be viewable at <http://your-username.github.io> or <http://your-username.github.io/your-favorite-name>.

### Step 2) Customize and view your site

Edit site info by editing the `_config.yml` file. 
Change `baseurl` to your repository's name.
If it is your-username.github.io then set it empty.

> There are 2 different ways that you can make changes to your blog's files:

> 1. Edit files within your new repository in the browser at gitHub.com (easiest).
> 2. Clone down your repository and make updates locally, then push them to your GitHub repository.

### Step 3) Publish your first blog post

Go to `/_posts/` and create a markdown file in this format: `year-month-day-title.md` to publish your first blog post. 

### Some manual setups

- You have to create `<new category name>.html` with the following content in the `category` folder when you create a new category.

```markdown
---
layout: category
title: new category name
category: new-category-name
---
```    

## Local Development

```shell
gem install jekyll bundler
bundle install
bundle exec jekyll serve
```

## How to import from wordpress

Install "WordPress to Jekyll Exporter"

Tools -> Export to Jekyll

Unzip the file and copy _posts, _config.yml, wp-content, and any .md files in the root to your repo.

```shell
cd ./_posts
# replace image links
find . -name '*.md' -print0 | xargs -0 sed -i "" "s/http:\/\/www.yourwebsite.com\/wp-content\/uploads/{{ site.baseurl }}/wp-content/uploads/g"
# replace code pre tags
find . -name '*.md' -print0 | xargs -0 sed -i "" "s/<pre>/<pre><code class=\"bash\">/g"
find . -name '*.md' -print0 | xargs -0 sed -i "" "s/<\/pre>/<\/code><\/pre>/g"
```
