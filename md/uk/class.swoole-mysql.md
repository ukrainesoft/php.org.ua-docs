---
navigation:
  - swoole-mmap.open.md: '« SwooleMmap::open'
  - swoole-mysql.close.md: 'SwooleMySQL::close »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
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

-   [SwooleMySQL::close](swoole-mysql.close.md) — Закриває асинхронне з'єднання MySQL
-   [SwooleMySQL::connect](swoole-mysql.connect.md) — Підключається до віддаленого сервера MySQL
-   [SwooleMySQL::construct](swoole-mysql.construct.md) - Створює асинхронний клієнт MySQL
-   [SwooleMySQL::destruct](swoole-mysql.destruct.md) - Знищує асинхронний клієнт MySQL
-   [SwooleMySQL::getBuffer](swoole-mysql.getbuffer.md) - Опис
-   [SwooleMySQL::on](swoole-mysql.on.md) - Реєструє callback-функцію на основі імені події
-   [SwooleMySQL::query](swoole-mysql.query.md) — Виконує запит SQL
