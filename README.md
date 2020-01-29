redis-mockify
============

Updated library forked from [redis-mock](https://github.com/yeahoffline/redis-mock) which is mocking the [node_redis](https://github.com/NodeRedis/node_redis).

# Installation

````bash
$ npm install redis-mockify --save-dev
````


## Usage

### node.js/io.js

The below code demonstrates a example of using the redis-mock client in node.js/io.js


```js
var redis = require("redis-mockify"),
    client = redis.createClient();
```


# API

Currently implemented are the following redis commands:

### General
* createClient
* duplicate
* auth
* end
* multi
  * exec
  * discard
  * exec_atomic
* batch

### Events
* ready
* connect
* end
* quit
* subscribe
* unsubscribe
* message
* psubscribe
* punsubscribe
* pmessage

### Publish/subscribe
* publish
* subscribe
* unsubscribe
* psubscribe
* punsubscribe

### Keys
* del
* keys
* scan
* exists
* type
* expire
* ttl
* incr
* incrby
* incrbyfloat
* decr
* decrby
* rename
* dbsize
* renamenx

### Strings
* get
* set
* append
* getset
* mget
* mset
* msetnx
* setex
* setnx
* ping

### Hashing
* hset
* hsetnx
* hget
* hexists
* hdel
* hlen
* hgetall
* hscan
* hmset
* hmget
* hkeys
* hvals
* hincrby
* hincrbyfloat

### Lists
* llen
* lpush
* rpush
* lpushx
* rpushx
* lpop
* rpop
* blpop
* brpop
* lindex
* lrange
* lrem
* lset

### Sets
* sadd
* srem
* smembers
* scard
* sismember

### Sorted Sets
* zadd
* zcard
* zcount
* zincrby
* zrange
* zrangebyscore
* zrank
* zrem
* zremrangebyrank
* zremrangebyscore
* zrevrange
* zrevrangebyscore
* zrevrank
* zunionstore (Partial: no support for `WEIGHTS` or `AGGREGATE` yet)
* zinterstore (Partial: no support for `WEIGHTS` or `AGGREGATE` yet)
* zscore

### Server
* flushdb
* flushall

## LICENSE - "MIT License"

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.
