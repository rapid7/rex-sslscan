# Rex::SSLScan

This library is a pure ruby implmenetation of the SSLScan tool originally written by Ian Ventura-Whiting. It currently depends on the system version of OpenSSL.
To be effective you will want to use this gem with a version of OpenSSL compiled to support the old versions of SSL and weak ciphers. We will be ivnestigating ways
to either prepackage a version of OpenSSL with this gem, or using an alternative in the future.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'rex-sslscan'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install rex-sslscan

## Usage

```
require 'rex-sslscan'

scanner = Rex::SSLScan::Scanner.new('192.168.1.1', 443)
results = scanner.scan
print_status results.to_s
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/rex-sslscan. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

