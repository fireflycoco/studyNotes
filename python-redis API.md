摘自：http://python.jobbole.com/87305/

```python
import redis
conn = redis.Redis(host='127.0.0.1', port=6379)
conn.set('name', 'coco')
conn.get('name')

#连接池
pool = redis.ConnectionPool(host='127.0.0.1', port=6379)
coon = redis.Redis(connection_pool=pool)
conn.set('name', 'coco')
```

# Global API
* delete(*names)
* exists(name)
* keys(pattern='*')
* rename(src, dst)
* move(name, db)
* randomkey()
* type(name)
* 

# String API
* set(name, value, ex=None, px=None, nx=False, xx=False)
* setex(name, value, time)
* psetex(name, time_ms, value)
* setnx(name, value)
* mset(*args, **kwargs)
* get(name)
* mget(keys, *args)
* getset(name,value)
* getrange(key, start, end)
* setrange(name, offset, value)
* setbit(name, offset, value)
* strlen(name)
* incr(name,amount=1)
* incrbyfloat(name, amount=1.0)
* decr(name, amount=1)
* append(key, value)

# Hash API
* hset(name, key, value)
* hmset(name, mapping)
* hget(name, key)
* hmget(name, keys, *args)
* hgetall(name)
* hlen(name)
* hkeys(name)
* hvals(name)
* hexists(name, key)
* hdel(name,*keys)
* hincrby(name, key, amount=1)
* hincrbyfloat(name, key, amount=1.0)
* hscan(name, cursor=0, match=None, count=None)
* expire(name, time)

# List API
* lpush(name, *values)
* rpush(name, *values)
* lpushx(name, value)
* rpushx(name, value)
* llen(name)
* linsert(name, where, refvalue, value)
* lset(name, index, value)
* lrem(name, value, num=0)
* lpop(name)
* rpop(name)
* lindex(name, index)
* lrange(name, start, end)
* ltrim(name, start, end)

# Set API
* sadd(name, *values)
* scard(name)
* sdiff(keys, *args)
* sdiffstore(dest, keys, *args)
* sinter(keys, *args)
* sinterstore(dest, keys, *args)
* sismember(name, value)
* smembers(name)
* smove(src, dst, value)
* spop(name)
* srandmember(name, number=None)
* srem(name, *values)
* sunion(keys, *args)
* sunionstore(dest, keys, *args)
* 