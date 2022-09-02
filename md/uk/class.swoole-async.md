---
navigation:
  - function.swoole-version.md: « swooleversion
  - swoole-async.dnslookup.md: 'SwooleAsync::dnsLookup »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleAsync
---
# Клас SwooleAsync

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

-   [SwooleAsync::dnsLookup](swoole-async.dnslookup.md) — Асинхронний та неблокуючий пошук IP на ім'я хоста
-   [SwooleAsync::read](swoole-async.read.md) - Асинхронне читання файлового потоку
-   [SwooleAsync::readFile](swoole-async.readfile.md) - Асинхронне читання файлу
-   [SwooleAsync::set](swoole-async.set.md) — Оновлює параметри асинхронного вводу-виводу
-   [SwooleAsync::write](swoole-async.write.md) — Асинхронно записує дані у файловий потік
-   [SwooleAsync::writeFile](swoole-async.writefile.md) - Опис
