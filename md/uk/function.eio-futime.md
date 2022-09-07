---
navigation:
  - function.eio-ftruncate.md: « eioftruncate
  - function.eio-get-event-stream.md: eiogeteventstream »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiofutime
---
# eiofutime

(PECL eio >= 0.0.1dev)

eiofutime — Змінює дату та час останньої модифікації та доступу до файлу

### Опис

```methodsynopsis
eio_futime(    mixed $fd,    float $atime,    float $mtime,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiofutime()** змінює дату та час останньої модифікації та доступу до файлу.

### Список параметрів

`fd`

Потік, покажчик на сокет, чи числовий дескриптор файлу, повернутий, наприклад, [eioopen()](function.eio-open.md)

`atime`

Час останнього доступу

`mtime`

Час останньої зміни

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, або **`null`**. Якщо передано **`null`**, то `pri` встановлюється в **`EIO_PRI_DEFAULT`**

`callback`

Функція `callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
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

**eiofutime()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eioutime()](function.eio-utime.md) - Змінює дату та час останньої модифікації та доступу до файлу
