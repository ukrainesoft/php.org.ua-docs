---
navigation:
  - function.eio-unlink.md: « eio\_unlink
  - function.eio-write.md: eio\_write »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_utime
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_utime

(PECL eio >= 0.0.1dev)

eio\_utime — Змінює дату та час останньої модифікації та доступу до файлу

### Опис

```methodsynopsis
eio_utime(    string $path,    float $atime,    float $mtime,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

### Список параметрів

`path`

Шлях до файлу.

`atime`

Час останнього доступу

`mtime`

Час останньої зміни

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, или\*\*`null`**. Якщо передано **`null`**, то`pri`устанавливается в**`EIO_PRI_DEFAULT`\*\*

`callback`

Функция`callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eio\_get\_last\_error()](function.eio-get-last-error.md)

`data`

Произвольная переменная, передаваемая в`callback`\-функцію.

### Значення, що повертаються

**eio\_utime()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_futime()](function.eio-futime.md) \- Змінює дату та час останньої модифікації та доступу до файлу
