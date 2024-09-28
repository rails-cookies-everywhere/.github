# Rails Cookies Everywhere

A collection of projects aiming to help developers use their [**Ruby on Rails**](https://github.com/rails/rails) authentication cookies in other apps.

Available languages/platforms:
- [JavaScript / NodeJS](https://github.com/rails-cookies-everywhere/rails-cookies-nodejs)
- [Rust](https://github.com/rails-cookies-everywhere/rails-cookies-rust)

Of course, lots of similar projects exist:
- [Haskell](https://github.com/iconnect/rails-session)
- [Elixir / Phoenix](https://github.com/cconstantin/plug_rails_cookie_session_store)
- [Go](https://github.com/adjust/gorails)
- [JavaScript / ExpressJS](https://github.com/clayzermk1/rails-cookie-parser)

## Decrypting cookies

The only major difference between Rails 5/6 and Rails 7 is the [hash digest used for key generation, which changed from Sha1 to Sha256](https://guides.rubyonrails.org/v7.1.3.2/upgrading_ruby_on_rails.html#digest-class-for-activesupport-digest-changing-to-sha256).

| Language   | Rails 5/6 |Rails 7 |
|------------|-----------|---------|
| JavaScript | ✅        | ❌      |
| Rust       | ✅        | ✅      |

## Encrypting cookies
The JavaScript library can encrypt cookies for Rails, but it's ill-advised to use.

## Basics and rules

- All libraries MUST work with the latest Rails defaults.
- When allowed by the language, all libraries should work "batteries included" by pulling the `SECRET_KEY_BASE` value from the `ENV`.
