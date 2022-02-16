---
layout: post
title:  "GitHub and Jekyll"
date:   2022-02-15 19:34:25 -0600
categories: jekyll notes
---

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


## Reference 

- [Installing Jekyll in MBA M1](https://alexmanrique.com/blog/development/2021/02/05/using-jekyll-in-macbook-air-m1.html)


## Default content

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
