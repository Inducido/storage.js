storage.js
==========

A simple wrapper for localStorage and sessionStorage access, with a in-memory object fallback if not present


storage.js exposes a simple API for cross browser local storage

```js
// Store 'mickey' at 'username'
storage.ls('username', 'mickey')
// or 
storage.local('username', 'mickey')

// Get 'username'
value=storage.ls('username')
value=storage.local('username')

// Remove 'username'
storage.remove('username')

// Store an object literal - storage.js uses JSON.stringify under the hood
storage.local('user', { name: 'marcus', age: 11 })

// Get the stored object - storage.js uses JSON.parse under the hood
var user = storage.get('user')
console.log(user)

```


How does it work?
------------------
storage.js uses localStorage or sessionStorage when available, and falls back on the userData behavior in IE6 and IE7. 
No cookies to fatten your network requests.

storage.js depends on JSON for serialization.
No JSON2.js dependacy, as pretty much all browsers that really matter in the year 2014+
Definitive list of browsers that support the JSON object look here: http://caniuse.com/json

Installation
------------
Just grab [storage.min.js] or [storage.js].


Contributors & Forks
--------------------
Inspired by: borrowed from https://gist.github.com/jed/966030 (in http://www.140byt.es)



Supported browsers
------------------
 - quickly tested on recent Firefox & chrome
 - todo

Storage limits
--------------
 - See http://dev-test.nemikor.com/web-storage/support-test/ for a list of limits per browser

Unsupported browsers
-------------------
 - todo




  [storage.min.js]: https://raw.github.com/marcuswestin/storage.js/master/storage.min.js
  [store+json2.min.js]: https://raw.github.com/marcuswestin/storage.js/master/store+json2.min.js
