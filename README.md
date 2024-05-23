# ExamityClient

Wrapper around the Examity scheduling API. A local test server for the API is included, run this with

```
puma -v -p 4567 config.ru
```

Example usage of TestApiServer:

```
curl -X POST -d  '{"clientId": "1", "secretKey": "2"}' \
  -H "Content-Type: application/json" http://localhost:4567/examity/api/token
```

Usage of the client:
```ruby
client = ExamityClient::Client.new do
  client_id = "your client id"
  secret_key = "your secret key"
end


## Installation

Add this line to your application's Gemfile:

```ruby
gem 'examity_client'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install examity_client

## Usage

    puma -v -p 4567 config.ru

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/Trueability/ta-examity-clientr.

## Copyright and Ownership

© 2024 Trueability

All code in this repository is owned and maintained by Trueability and is provided under the terms of the MIT License. By contributing to this repository, you agree that your contributions will be licensed under the same license.
