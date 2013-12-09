# OmniAuth Bigcommerce Strategy
[![Build Status](https://travis-ci.org/bigcommerce/omniauth-bigcommerce.png?branch=master)](https://travis-ci.org/bigcommerce/omniauth-bigcommerce)

This gem provides a dead simple way to authenticate to Bigcommerce using OmniAuth.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'omniauth-bigcommerce'
```

## Usage

First, you will need to [register an application](https://developers.bigcommerceapp.com).

```ruby
use OmniAuth::Builder do
provider :bigcommerce, ENV['your_client_id'], ENV['your_client_secret'], 'list_of_scopes, api_v2_all'
end
```

## Auth Hash Schema

The following information is provided back to you for this provider:

```ruby
{
  uid: '12345',
  info: {
    username: 'someone@example.com',
    email: 'someone@example.com'
  },
  credentials: {
    token: 'xyz123abc'
  },
  extra: {
    raw_info: raw_api_response,
    scopes: 'requested_scopes'
  }
}
```

## Contributing

Fork & submit a pull request.
