# Tech. Notes

* [Installing Jekyll in MBA M1](https://alexmanrique.com/blog/development/2021/02/05/using-jekyll-in-macbook-air-m1.html)

## My Steps to install Jekyll

brew install rbenv
rbenv install 3.0.0
rbenv global 3.0.0

[.zshrc]
export PATH="$HOME/.gem/ruby/3.0.0/bin:$PATH"
eval "$(rbenv init - zsh)"


gem install --user-install rails
gem install --user-install ffi
gem install --user-install bundler jekyll

jekyll new myblog
cd myblog
bundle add webrick

bundle exec jekyll serve

