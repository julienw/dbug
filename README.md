# dbug

A drop-in replacement for [debug][], for slightly more utility.

```js
var dbug = require('dbug')('foo:bar');

dbug('just like debug'); // except goes to stdout, not stderr
dbug(new Error('also like debug'));

// additional methods
dbug.info('info');
dbug.warn('warning');
dbug.error('red alert');
```

Just like debug, `dbug` won't do anything unless the `DEBUG` env variable matches the `dbug` logger, but with slightly more lenient matching.

```
DEBUG=*
DEBUG=foo,quux
DEBUG=foo // also acts as foo:*
```

[debug]: https://npmjs.org/package/debug
