---
navigation:
  - function.eio-unlink.md: « eiounlink
  - function.eio-write.md: eiowrite »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eioutime
---
# eioutime

(PECL eio >= 0.0.1dev)

eioutime — Змінює дату та час останньої модифікації та доступу до файлу

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

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, або **`null`**. Якщо передано **`null`**, то `pri` встановлюється в **`EIO_PRI_DEFAULT`**

`callback`

Функція `callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.md)

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

**eioutime()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eiofutime()](function.eio-futime.md) - Змінює дату та час останньої модифікації та доступу до файлу
