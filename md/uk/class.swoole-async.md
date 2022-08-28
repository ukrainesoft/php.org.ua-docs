Клас SwooleAsync

-   [« swoole\_version](function.swoole-version.html)
    
-   [Swoole\\Async::dnsLookup »](swoole-async.dnslookup.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleAsync
    

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

-   [Swoole\\Async::dnsLookup](swoole-async.dnslookup.html) — Асинхронний та неблокуючий пошук IP на ім'я хоста
-   [Swoole\\Async::read](swoole-async.read.html) - Асинхронне читання файлового потоку
-   [Swoole\\Async::readFile](swoole-async.readfile.html) - Асинхронне читання файлу
-   [Swoole\\Async::set](swoole-async.set.html) — Оновлює параметри асинхронного вводу-виводу
-   [Swoole\\Async::write](swoole-async.write.html) — Асинхронно записує дані у файловий потік
-   [Swoole\\Async::writeFile](swoole-async.writefile.html) - Опис