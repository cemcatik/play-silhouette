## 4.0

- Removed Play Messages instance from Event, Authorization and ErrorHandler types. The I18nSupport trait should be used instead, to get the Messages instance for the current request
- Rewrite Silhouette trait to provide injectable actions (this is now the default method from Play 2.5 on)
  - Every SecuredAction can now override the global(default injected) error handler if needed
  - A controller is not bound to a single Authenticator anymore
- Remove SecuredErrorHandler in favour of injectable error handler

## 3.0 (2015-07-14)

- Update to Play 2.4
- Stateless and non-stateless CookieAuthenticator
- Allow to customize the Gravatar service
- Use scala.concurrent.duration.FiniteDuration instead of Int for duration based values
- A lot of API enhancements

## 2.0 (2015-03-28)

- Use lazy val to initialize SecureRandom, so that initialization occurs also async
- Refactor authenticators and add BearerTokenAuthenticator, JWTAuthenticator, SessionAuthenticator and DummyAuthenticator
- Better error handling for authenticators
- Authenticators now using an extra backing store instead of only the cache
- Split up SocialProvider.authenticate method into authenticate and retrieveProfile methods
- Remove authInfo from SocialProfile
- Add OAuth1 token secret implementation
- Add OAuth2 state implementation
- Documentation is now included in the repository and hosted on Read The Docs
- Renamed packages "core" to "api", "contrib" to "impl", "utils" to "util"
- Reorganized the project structure (moved all providers into the "impl" package, moved some classes/traits)
- Add request handlers
- Add request providers in combination with HTTP basic auth provider
- Add Dropbox provider
- Add Clef provider
- Add request extractors
- Better social profile builder implementation
- Add OpenID providers Steam and Yahoo
- Better error handling

## 1.0 (2014-06-12)

- First release for Play 2.3

## 0.9 (2014-06-12)

- First release for Play 2.2
