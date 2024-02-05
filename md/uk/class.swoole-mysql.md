---
navigation:
  - swoole-mmap.open.md: '« Swoole\\Mmap::open'
  - swoole-mysql.close.md: 'Swoole\\MySQL::close »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\MySQL
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\MySQL

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

-   [Swoole\\MySQL::close](swoole-mysql.close.md)— Закриває асинхронне з'єднання MySQL
-   [Swoole\\MySQL::connect](swoole-mysql.connect.md)— Підключається до віддаленого сервера MySQL
-   [Swoole\\MySQL::\_\_construct](swoole-mysql.construct.md) \- Створює асинхронний клієнт MySQL
-   [Swoole\\MySQL::\_\_destruct](swoole-mysql.destruct.md) \- Знищує асинхронний клієнт MySQL
-   [Swoole\\MySQL::getBuffer](swoole-mysql.getbuffer.md) \- Опис
-   [Swoole\\MySQL::on](swoole-mysql.on.md) \- Реєструє callback-функцію на основі імені події
-   [Swoole\\MySQL::query](swoole-mysql.query.md)— Виконує запит SQL
