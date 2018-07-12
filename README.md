# JihunDev.github.io
Jekyll & Minimal Mistakes 

## Getting Started
### Requirements
- Jekyll
- Minimal Mistakes

### Installation

#### Set up Ruby included with the OS
```
$ gem install bundler jekyll

# Create a Gemfile
$ bundle init

# Add Jekyll
$ bundle add jekyll

# Install gems
$ bundle install
```

#### Install a newer Ruby version via Homebrew
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

$ brew install ruby

$ ruby -v
ruby 2.5.1p57 (2018-03-29 revision 63029) [x86_64-darwin17]
```

#### Install multiple Ruby versions with rbenvPermalink
```
# Install rbenv and ruby-build
$ brew install rbenv

# Setup rbenv integration to your shell
$ rbenv init

# Check your install
$ curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor | bash

$ rbenv install 2.5.1

$ rbenv global 2.5.1

$ ruby -v
ruby 2.5.1p57 (2018-03-29 revision 63029) [x86_64-darwin17]
```

#### Minimal Mistakes Theme 적용
[Minimal Mistakes Github](https://github.com/mmistakes/minimal-mistakes/) 다운로드 후 압축 해제한 파일을 Jekyll 폴더에 넣기

### Usage

#### 192.0.0.1:4000 접속하여 확인
```
$ bundle exec jekyll seve
```


### Development
[jekyll](https://jekyllrb-ko.github.io)

[Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)


## License

This project is licensed under the MIT License - see [LICENSE.md](LICENSE.md) file for details.
