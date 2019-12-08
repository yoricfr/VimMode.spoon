# Setting up to run integration tests

The integration tests require a few things up front to run:

```
brew install chromedriver
```

Next, you'll have to deal with some first-run crap, in order to give
`osascript` permissions. This is the only way I could figure out how to give
RSpec the ability to send native OS X keys. If there is a way to do this
without needing permissions, please open a PR/issue!

```
bundle install
bundle exec rspec spec
```

It will ask for permissions for `System Events.app`, you'll need to give them:

![](https://user-images.githubusercontent.com/59429/70395829-c00cdf00-19b7-11ea-91c2-50cefe25b329.png)