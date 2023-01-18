# Superclient

One client to rule them all. Superclient queries all kinds of endpoints. Interacts with REST, SOAP and gRPC endpoints.

## Installation

Install the gem and add to the application's Gemfile by executing:

    $ bundle add superclient

If bundler is not being used to manage dependencies, install the gem by executing:

    $ gem install superclient

## Usage

Example of how it works for queries in XML SOAP, protobuf, and HTTP endpoints;

```ruby
require 'superclient'

client = Superclient.new
client.configure do |config|
  config.endpoint = 'https://example.com'
  config.format = :xml
end

response = client.query('get_data', {param1: 'value1', param2: 'value2'})

# To query protobuf endpoint
client.configure do |config|
  config.endpoint = 'https://example.com'
  config.format = :protobuf
end

response = client.query('get_data', {param1: 'value1', param2: 'value2'})

# To query http endpoint
client.configure do |config|
  config.endpoint = 'https://example.com'
  config.format = :http
end

response = client.query('get_data', {param1: 'value1', param2: 'value2'})
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and the created tag, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/Sylvance/superclient. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [code of conduct](https://github.com/Sylvance/superclient/blob/main/CODE_OF_CONDUCT.md).

## Code of Conduct

Everyone interacting in the Superclient project's codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/Sylvance/superclient/blob/main/CODE_OF_CONDUCT.md).
