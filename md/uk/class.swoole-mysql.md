---
navigation:
  - swoole-mmap.open.html: '« SwooleMmap::open'
  - swoole-mysql.close.html: 'SwooleMySQL::close »'
  - index.html: PHP Manual
  - book.swoole.html: Swoole
title: Клас SwooleMySQL
---
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

-   [SwooleMySQL::close](swoole-mysql.close.html) — Закриває асинхронне з'єднання MySQL
-   [SwooleMySQL::connect](swoole-mysql.connect.html) — Підключається до віддаленого сервера MySQL
-   [SwooleMySQL::construct](swoole-mysql.construct.html) - Створює асинхронний клієнт MySQL
-   [SwooleMySQL::destruct](swoole-mysql.destruct.html) - Знищує асинхронний клієнт MySQL
-   [SwooleMySQL::getBuffer](swoole-mysql.getbuffer.html) - Опис
-   [SwooleMySQL::on](swoole-mysql.on.html) - Реєструє callback-функцію на основі імені події
-   [SwooleMySQL::query](swoole-mysql.query.html) — Виконує запит SQL
