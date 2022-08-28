Записує кеш із буфера на диск

-   [« eio\_sync\_file\_range](function.eio-sync-file-range.html)
    
-   [eio\_syncfs »](function.eio-syncfs.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Записує кеш із буфера на диск
    

# eiosync

(PECL eio >= 0.0.1dev)

eiosync — записує кеш із буфера на диск

### Опис

```methodsynopsis
eio_sync(int $pri = EIO_PRI_DEFAULT, callable $callback = NULL, mixed $data = NULL): resource
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eiosync()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.