Клас SwooleMySQL

-   [« Swoole\\Mmap::open](swoole-mmap.open.html)
    
-   [Swoole\\MySQL::close »](swoole-mysql.close.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleMySQL
    

# Клас SwooleMySQL

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\MySQL
     
     {


    /* Методы */
    
   public close(): void
public connect(array $server_config, callable $callback): void
public __destruct(): void
public getBuffer(): ReturnType
public on(string $event_name, callable $callback): void
public query(string $sql, callable $callback): ReturnType

   }
```

## Зміст

-   [Swoole\\MySQL::close](swoole-mysql.close.html) — Закриває асинхронне з'єднання MySQL
-   [Swoole\\MySQL::connect](swoole-mysql.connect.html) — Підключається до віддаленого сервера MySQL
-   [Swoole\\MySQL::\_\_construct](swoole-mysql.construct.html) - Створює асинхронний клієнт MySQL
-   [Swoole\\MySQL::\_\_destruct](swoole-mysql.destruct.html) - Знищує асинхронний клієнт MySQL
-   [Swoole\\MySQL::getBuffer](swoole-mysql.getbuffer.html) - Опис
-   [Swoole\\MySQL::on](swoole-mysql.on.html) - Реєструє callback-функцію на основі імені події
-   [Swoole\\MySQL::query](swoole-mysql.query.html) — Виконує запит SQL