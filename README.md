# Joe's Blog

## Issues last time
Last time i ran into issues installing Jekyll (similar to https://github.com/netlify-templates/jekyll-netlify-cms/issues/8). However, I got it to successfully run using `bundle upgrade`. I was then able to use `make server` to get things started. Using ruby 2.5.1

## Install

See: https://jekyllrb.com/docs/quickstart/

```bash
brew install rbenv ruby-build
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
source ~/.bash_profile
rbenv install 2.5.1
rbenv global 2.5.1
ruby -v
# open new terminal
gem install jekyll bundler
bundle install
```

## Trouble-shooting

```bash
brew update && brew upgrade
brew doctor
brew uninstall --force ruby
brew install ruby
# close and reopen terminal
```

Big guns:

```bash

sudo chown -R $(whoami) /usr/local/lib/ruby/*
sudo chown -R $(whoami) /Library/Ruby/Gems/2.0.0
brew link ruby
```

## Run the server

```bash
make server
```
