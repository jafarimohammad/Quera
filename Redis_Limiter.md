سلیب که به تازگی با داکر آشنا شده قصد دارد تا یک docker-compose ابتدایی را طراحی کند. در ادامه به بیان جزئیات کانتینر مورد نظر او می‌پردازیم، به سلیب کمک کنید محدویت‌های زیر را در منابع یک container داکر Redis اضافه کند:

او می‌خواهد تا Redis روی پورت 6379 اجرا شده باشد.
هرگاه به هردلیلی سرویس Redis از کار افتاد، بلافاصله مجددا اجرا شود.
دارای Memory Limit‌ای برابر با 30M باشد.
دارای Memory Reservation‌ای برابر با 30M باشد.

```
version: "2"
services:
 limited_redis:
  image: registry.gitlab.com/qio/standard/redis:latest
  ports:
   - 6379:6379
  restart: always
  mem_limit: 30M
  mem_reservation: 30M
```
