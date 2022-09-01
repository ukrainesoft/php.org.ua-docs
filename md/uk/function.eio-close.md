---
navigation:
  - function.eio-chown.html: « eiochown
  - function.eio-custom.html: eiocustom »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eioclose
---
# eioclose

(PECL eio >= 0.0.1dev)

eioclose — Закрити файл

### Опис

```methodsynopsis
eio_close(    mixed $fd,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eioclose()** закриває файл, вказаний у `fd`

### Список параметрів

`fd`

Потік, покажчик на сокет (Socket resource), чи числовий дескриптор файлу

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

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.html)

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

**eioclose()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eioopen()](function.eio-open.html) - Відкриває файл
