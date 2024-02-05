---
navigation:
  - function.eio-symlink.md: « eio\_symlink
  - function.eio-sync.md: eio\_sync »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_sync\_file\_range
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_sync\_file\_range

(PECL eio >= 0.0.1dev)

eio\_sync\_file\_range — Синхронізує сегмент файлу із даними файлу на зовнішньому сховищі

### Опис

```methodsynopsis
eio_sync_file_range(    mixed $fd,    int $offset,    int $nbytes,    int $flags,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_sync\_file\_range()** здійснює необхідні перевірки та дії при синхронізації відкритого файлу `fd` з дисковою підсистемою.

### Список параметрів

`fd`

Файловий описувач

`offset`

Початкова позиція, з якою проводитиметься синхронізація

`nbytes`

Задає довжину сегмента файлу в байтах, яку потрібно синхронізувати. Якщо `nbytes` і нулю, будуть синхронізовані всі дані від `offset`до конца файла.

`flags`

Бітова маска. Може включати комбінацію з наступних значень: **`EIO_SYNC_FILE_RANGE_WAIT_BEFORE`** **`EIO_SYNC_FILE_RANGE_WRITE`** **`EIO_SYNC_FILE_RANGE_WAIT_AFTER`**. Ці прапори мають те саме призначення, що й аналогічні *SYNC\_FILE\_RANGE\_\** константи (дивіться сторінку керівництва `SYNC_FILE_RANGE(2)`

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

Дані, які потрібно передати функції `callback`

### Значення, що повертаються

**eio\_sync\_file\_range()** повертає ресурс запиту у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
