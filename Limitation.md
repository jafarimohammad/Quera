# Resource limitations:
```
version: "2"
services:
 limited_redis:
  image: registry.gitlab.com/qio/standard/redis:latest
  mem_limit: 30M
  cpu_shares: 70
  ```
