Inside the `Setup` methods several assumptions are made:

If `$isDevMode` is true caching is done in memory with the ArrayCache. Proxy objects are recreated on every request.

If `$isDevMode` is false, check for Caches in the order APC, Xcache, Memcache (127.0.0.1:11211), Redis (127.0.0.1:6379) unless `$cache` is passed as fourth argument.

If `$isDevMode` is false, set then proxy classes have to be explicitly created through the command line.

If third argument `$proxyDir` is not set, use the systems temporary directory.
