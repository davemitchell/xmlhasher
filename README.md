# XmlHasher

[![Build Status](https://travis-ci.org/cloocher/xmlhasher.png)](https://travis-ci.org/cloocher/xmlhasher)
[![Coverage Status](https://coveralls.io/repos/cloocher/xmlhasher/badge.png?branch=master)](https://coveralls.io/r/cloocher/xmlhasher)
[![Gem Version](https://badge.fury.io/rb/xmlhasher.png)](http://badge.fury.io/rb/xmlhasher)

Fast XML to Ruby Hash converter

## Installation

## Installation

Aggcat is available through [Rubygems](http://rubygems.org/gems/xmlhasher) and can be installed via:

```
$ gem install xmlhasher
```

or add it to your Gemfile like this:

```
gem 'xmlhasher'
```

## Usage

```ruby
require 'xmlhasher'

# XmlHasher global configuration
XmlHasher.configure do |config|
  config.snakecase = true
  config.ignore_namespaces = true
end

# alternatively, specify configuration options when instantiating a Parser
parser = XmlHasher::Parser.new(
  :snakecase => true,
  :ignore_namespaces => true
)

# parse XML file
XmlHasher.parse(File.new('/path/to/my/file.xml'))

# parse XML string
XmlHasher.parse(xml)

```
