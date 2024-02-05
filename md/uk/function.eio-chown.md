---
navigation:
  - function.eio-chmod.md: « eio\_chmod
  - function.eio-close.md: eio\_close »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_chown
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_chown

(PECL eio >= 0.0.1dev)

eio\_chown — Змінює права доступу до файлу/директорії

### Опис

```methodsynopsis
eio_chown(    string $path,    int $uid,    int $gid = -1,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

Змінює права доступу до файлу/директорії.

### Список параметрів

`path`

Шлях до файлу чи директорії.

**Увага**

Уникайте відносних шляхів

`uid`

Код користувача. Ігнорується при значенні, що дорівнює -1.

`gid`

Код групи. Ігнорується при значенні, що дорівнює -1.

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

**eio\_chown()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_chmod()](function.eio-chmod.md) \- Змінює права доступу до файлу/директорії
