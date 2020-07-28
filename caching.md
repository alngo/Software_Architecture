#### Caching

>Caching is key to the performance of any kind of application. It ensures low latency and high throughput. An application with caching will certainly do better than an application without caching, simply because it returns the response in less time as opposed to the application without a cache implemented.

Copying frequently accessed data to RAM -> faster access

Cache dynamic data (cache invalidation -> jwt token?)
Cache static data -> img, font file, css, etc... this  (client side)

Cache with key:value

[HTTP cache](https://web.dev/http-cache/)

Note: Sometime -> Reduce application cost with cache

#### Strategy

##### Cache Aside
User request -> look data in the cache first (data ? return data : retrieve data from database )
Eventually Consistent => TTL to refresh the data in cache
##### Read-through cache
Similar to cache aside but
Consistent with database => backend update the cache on request
##### Write-through cache
each & every information written to the database goes through the cache
High consitency
##### Write-back cache
data is writtent in the cache then after a delay in the db => reduce the database write

