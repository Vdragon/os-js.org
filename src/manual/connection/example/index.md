---
title: Connection Example
layout: layout.html
---

# Connection Example

## Server

See the [included example](https://github.com/os-js/OS.js/blob/master/src/server/node/modules/connection/example.js) for a full template.

## Client

In this example we use the default HTTP backend, but modify the API request:

```js
(function(_super) {
  function MyConnection() {
    _super(this, arguments);
  }

  MyConnection.prototype = Object.create(_super.prototype);
  MyConnection.constructor = _super;

  // An example method for adding headers to the requests
  MyConnection.prototype.request = function(method, args, onsuccess, onerror, options) {
    options = options || {};

    // See 'Utils.ajax()' for more info
    options.requestHeaders = {
      'X-Custom-Header': 'Some fancy value'
    };

    // Let the base class finish the job
    return _super.prototype.request.call(method, args, options, onsuccess, onerror);
  };

})(OSjs.Connections.http);

```