---
navigation:
  - function.swoole-version.md: « swoole\_version
  - swoole-async.dnslookup.md: 'Swoole\\Async::dnsLookup »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Async
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Async

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Async
     
     {


    /* Методы */
    
   public static dnsLookup(string $hostname, callable $callback): void
public static read(    string $filename,    callable $callback,    int $chunk_size = ?,    int $offset = ?): bool
public static readFile(string $filename, callable $callback): void
public static set(array $settings): void
public static write(    string $filename,    string $content,    int $offset = ?,    callable $callback = ?): void
public static writeFile(    string $filename,    string $content,    callable $callback = ?,    string $flags = ?): void

   }
```

## Зміст

-   [Swoole\\Async::dnsLookup](swoole-async.dnslookup.md)— Асинхронний та неблокуючий пошук IP на ім'я хоста
-   [Swoole\\Async::read](swoole-async.read.md) \- Асинхронне читання файлового потоку
-   [Swoole\\Async::readFile](swoole-async.readfile.md) \- Асинхронне читання файлу
-   [Swoole\\Async::set](swoole-async.set.md)— Оновлює параметри асинхронного вводу-виводу
-   [Swoole\\Async::write](swoole-async.write.md)— Асинхронно записує дані у файловий потік
-   [Swoole\\Async::writeFile](swoole-async.writefile.md) \- Опис
