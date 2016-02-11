# Garner + Grape API Caching

### A Basic Ruby Grape APP

Create a `Gemfile`.

```ruby
source 'http://rubygems.org'

gem 'grape'
```

Create an API.

```ruby
require 'grape'

class API < Grape::API
  format :json

  get do
    { count: 1 }
  end
end

run API
```

Try it.

```
$ rackup
[2016-02-11 08:11:57] INFO  WEBrick 1.3.1
[2016-02-11 08:11:57] INFO  ruby 2.2.1 (2015-02-26) [x86_64-darwin15]
[2016-02-11 08:11:57] INFO  WEBrick::HTTPServer#start: pid=98509 port=9292
```

Curl it.

```
$ curl localhost:9292
{"count":1}
```
