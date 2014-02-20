*This repository is a mirror of the [component](http://component.io) module [nk-components/request-timeout](http://github.com/nk-components/request-timeout). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/nk-components-request-timeout`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# request-timeout

  Like setTimeout() but with requestAnimationFrame()

  > setTimeout doesn’t take into account what else is happening in the browser.  
  > [Source](http://creativejs.com/resources/requestanimationframe/)
  
  You can also find `requestInterval` component [here](https://github.com/nk-components/request-interval).
  
## Installation

  Install with [component(1)](http://component.io):

    $ component install nk-components/request-timeout

## API

    var requestTimeout = require('request-timeout');

    requestTimeout(300, function() {
      // do something
    });

    var id = requestTimeout(300, function() {
      console.log('should not be executed');
    });

    setTimeout(function() {
      requestTimeout.clear(id);
    }, 100);

## License

  MIT
  
  Inspired by [Joe Lambert's Gist](https://gist.github.com/joelambert/1002116#file-requesttimeout-js).
