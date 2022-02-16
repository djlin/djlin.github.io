---
layout: page
title: Tech. Notes
permalink: /notes
---

# Tech. Notes

* [Installing Jekyll in MBA M1](https://alexmanrique.com/blog/development/2021/02/05/using-jekyll-in-macbook-air-m1.html)

## My steps to install Jekyll

		brew install rbenv
		rbenv install 3.0.0
		rbenv global 3.0.0

* **.zshrc**

		export PATH="$HOME/.gem/ruby/3.0.0/bin:$PATH"
		eval "$(rbenv init - zsh)"

* **Commands**

		gem install --user-install rails
		gem install --user-install ffi
		gem install --user-install bundler jekyll

		jekyll new myblog
		cd myblog
		bundle add webrick
		bundle install

		bundle exec jekyll serve

* [Creating a GitHub Pages site with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll)

1. Create [GitHub ID].github.io repo

		mkdir docs; cd docs
		jekyll new --skip-bundle .

2. Edit Gemfile and comment out **gem "jekyll"**

3. Add the following (See ["Dependency versions."](https://pages.github.com/versions/))

		gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins

4. Edit **_config.yml**
 
		domain: [GitHub ID].github.io
		url: https://[GitHub ID].github.io
		baseurl: /REPO-NAME/

## Test Page with Jykell

- Go to the folder of the page

		bundle install
		bundle add webrick
		bundle exec jykell serve

- Navigate to [http://localhost:4000](http://localhost:4000).
