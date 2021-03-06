# fit [![Build Status](https://travis-ci.org/tjwallace/fit.svg?branch=master)](https://travis-ci.org/tjwallace/fit)

A ruby gem for parsing [fit files](http://www.thisisant.com/pages/products/fit-sdk). It makes heavy use of the [bindata gem](http://bindata.rubyforge.org/).

It is published on RubyGems.org as [fit-parser](https://rubygems.org/gems/fit-parser).

## Example usage

```ruby
require 'fit'

fit_file = Fit.load_file(ARGV[0])

records = fit_file.records.select{ |r| r.content.record_type != :definition }.map{ |r| r.content }
```

## Supported files

This library has been tested with files coming from the following devices:
  - Garmin Swim
  - Garmin Forerunner 35


Please let me know if you have any success with files coming from devices that are not listed here.

## Contributing to fit
 
* Check out the latest master to make sure the feature hasn't been implemented or the bug hasn't been fixed yet
* Check out the issue tracker to make sure someone already hasn't requested it and/or contributed it
* Fork the project
* Start a feature/bugfix branch
* Commit and push until you are happy with your contribution
* Make sure to add tests for it. This is important so I don't break it in a future version unintentionally.
* Please try not to mess with the Rakefile, version, or history. If you want to have your own version, or is otherwise necessary, that is fine, but please isolate to its own commit so I can cherry-pick around it.

## Copyright

Copyright (c) 2015 Jeff Wallace. See LICENSE.txt for further details.
