---
navigation:
  - function.eio-sync-file-range.md: « eio\_sync\_file\_range
  - function.eio-syncfs.md: eio\_syncfs »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_sync
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_sync

(PECL eio >= 0.0.1dev)

eio\_sync — записує кеш із буфера на диск

### Опис

```methodsynopsis
eio_sync(int $pri = EIO_PRI_DEFAULT, callable $callback = NULL, mixed $data = NULL): resource
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eio\_sync()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
