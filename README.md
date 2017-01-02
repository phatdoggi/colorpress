# colorpress

When you turn the character data of a file into pixel data in a PNG image, the result is a neat kind of compression.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'colorpress'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install colorpress

## Usage

Encode bytes of a file to PNG format:
```ruby
Colorpress::PNG.encode('file.txt') # creates file.txt.png
Colorpress::PNG.encode('file.txt', 'out.png') # creates out.png
```
Decode bytes of a PNG back into character data:
```ruby
Colorpress::PNG.decode('file.txt.png') # creates file.txt, deletes file.txt.png
Colorpress::PNG.decode('file.txt.png', cleanup=false) # creates file.txt, keeps file.txt.png
Colorpress::PNG.decode('out.png', 'original.txt') # creates original.txt, deletes out.png
```
Documentation for all methods can be generated by running `yard doc` in a development environment.

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/lucis-fluxum/colorpress. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org/) code of conduct.

