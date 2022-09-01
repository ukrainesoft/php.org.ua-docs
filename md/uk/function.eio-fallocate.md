---
navigation:
  - function.eio-event-loop.html: « eioeventloop
  - function.eio-fchmod.html: eiofchmod »
  - index.html: PHP Manual
  - ref.eio.html: Eio Функции
title: eiofallocate
---
# eiofallocate

(PECL eio >= 0.0.1dev)

eiofallocate — Дозволяє безпосередньо керувати розміром дискового простору, що використовується для файлу.

### Опис

```methodsynopsis
eio_fallocate(    mixed $fd,    int $mode,    int $offset,    int $length,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiofallocate()** дозволяє безпосередньо керувати розміром дискового простору для файлу. Дескриптор файлу вказується у параметрі `fd`, Розмір визначається діапазоном в байтах, починаючи від зсуву `offset` і до `length`

> **Зауваження** **Файл має бути відкритим для запису**
> 
> **`EIO_O_CREAT`** *ВР* (одна з констант **`EIO_O_WRONLY`** **`EIO_O_RDWR`**

### Список параметрів

`fd`

Потік, покажчик на сокет, чи числовий дескриптор файлу, наприклад повернутий [eioopen()](function.eio-open.html)

`mode`

Доступний лише один прапор: **`EIO_FALLOC_FL_KEEP_SIZE`** (те саме, що **`FALLOC_FL_KEEP_SIZE`** в POSIX).

`offset`

Визначає усунення діапазону в байтах.

`length`

Визначає розміри діапазону.

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

**eiofallocate()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.
