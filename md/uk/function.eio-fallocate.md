---
navigation:
  - function.eio-event-loop.md: « eio\_event\_loop
  - function.eio-fchmod.md: eio\_fchmod »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_fallocate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_fallocate

(PECL eio >= 0.0.1dev)

eio\_fallocate — Дозволяє безпосередньо керувати розміром дискового простору, що використовується для файлу.

### Опис

```methodsynopsis
eio_fallocate(    mixed $fd,    int $mode,    int $offset,    int $length,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_fallocate()** дозволяє безпосередньо керувати розміром дискового простору для файлу. Дескриптор файлу вказується у параметрі `fd`, Розмір визначається діапазоном в байтах, починаючи від зсуву `offset`и до`length`

> **Зауваження** **Файл має бути відкритим для запису**
> 
> **`EIO_O_CREAT`** *OR*(одна из констант\*\*`EIO_O_WRONLY`\*\* **`EIO_O_RDWR`**

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу, наприклад повернутий [eio\_open()](function.eio-open.md)

`mode`

Доступний лише один прапор: **`EIO_FALLOC_FL_KEEP_SIZE`** (те саме, що \*\*`FALLOC_FL_KEEP_SIZE`\*\*в POSIX).

`offset`

Визначає усунення діапазону в байтах.

`length`

Визначає розміри діапазону.

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

**eio\_fallocate()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
