# makeitping-cloud

## Building the website on MacOS

Install the latest ruby:

```
brew install ruby
echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> /Users/awsandy/.bash_profile
. ~/.bash_profile
ruby -v
ruby 2.7.1p83 (2020-03-31 revision a0c7c23c9c) [x86_64-darwin18]
```

Install Jekyll

```
gem install --user-install bundler jekyll jekyll-include-cache
echo 'export PATH="$HOME/.gem/ruby/2.7.0/bin:$PATH"' >> ~/.bash_profile
gem -v
3.1.2
gem env
```

From the docs folder:

Add this line to the Gemfile
```
gem 'jekyll-include-cache'
```


```
bundle install
```

Develop/Tets locally on localhost:4000

```
bundle exec jekyll serve
```


Deployment:
```
bundle exec jekyll build
```

The above creates static content in _site (copy to S3 or your web site)



Reference:

https://jekyllrb.com/docs/installation/macos/