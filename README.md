# OmniAuth::OpenIDConnect
OpenID Connect strategy for OmniAuth
[![Gem Version](https://badge.fury.io/rb/omniauth-openid-reconnect.png)](http://badge.fury.io/rb/omniauth-openid-reconnect)
[![Build Status](https://travis-ci.org/thinkthroughmath/omniauth-openid-reconnect.svg?branch=master)](https://travis-ci.org/thinkthroughmath/omniauth-openid-reconnect)
[![Coverage Status](https://coveralls.io/repos/thinkthroughmath/omniauth-openid-reconnect/badge.png?branch=master)](https://coveralls.io/r/thinkthroughmath/omniauth-openid-reconnect?branch=master)
[![Code Climate](https://codeclimate.com/github/thinkthroughmath/omniauth-openid-reconnect.png)](https://codeclimate.com/github/thinkthroughmath/omniauth-openid-reconnect)

## Background

This is derrived work from `jjbohn/omniauth-openid-connect` which appears to be abandoned at this point. I have continued to merge PR's placed against that repo. But I have added enough of my own changes that it is diverged enough to re-release. @ThinkThroughMath actively utilizes this strategy and we will do our best to maintain it.

### Whats different.

- Using Addressable 2.2.8 - In 2.3+ `addressable` decided that the way that Rails 3 handles param[] items was too hard to handle and removed the feature. This breaking change within a semantic version makes using addressable > 2.3 difficult in existing applications. There is no impact on the auth strategy though.
- Better devise support be returning a default `name` options parameter
- Partial integration of google `nonce` requirement.
- Inclusing of aging PRs from the parent gem this replaces.

## Installation

Add this line to your application's Gemfile:

    gem 'omniauth-openid-reconnect'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install omniauth-openid-reconnect

## Usage

Example configuration
```ruby
config.omniauth :openid_connect, {
  scope: [:openid, :email, :profile, :address],
  response_type: :code,
  client_options: {
    port: 443,
    scheme: "https",
    host: "myprovider.com",
    identifier: ENV["OP_CLIENT_ID"],
    secret: ENV["OP_SECRET_KEY"],
    redirect_uri: "http://myapp.com/users/auth/openid_connect/callback",
  },
}
```

Configuration details:
  * `name` is an optional requirement as of `omniauth-1.2` but it does have an effect with dealing with devise and is the base for which devise uses to create routes identified with `devise_for`. The default is set to the expected camelization of `openid_connect`. If you need to override it you can pass the `name` parameter to the config hash. **Be aware** that what you set this to will be the provider for your devise routes.
  * Although `response_type` is an available option, currently, only `:code`
  is valid. There are plans to bring in implicit flow and hybrid flow at some
  point, but it hasn't come up yet for me. Those flows aren't best practive for
  server side web apps anyway and are designed more for native/mobile apps.

For the full low down on OpenID Connect, please check out
[the spec](http://openid.net/specs/openid-connect-core-1_0.html).

## Contributing

1. Fork it ( http://github.com/thinkthroughmath/omniauth-openid-reconnect/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
