---
navigation:
  - function.yaz-errno.md: « yaz\_errno
  - function.yaz-es-result.md: yaz\_es\_result »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_error

(PHP 4 >= 4.0.1, PECL yaz >= 0.9.0)

yaz\_error — Повертає опис помилки

### Опис

```methodsynopsis
yaz_error(resource $id): string
```

**yaz\_error()** повертає текстове повідомлення англійською мовою, що відповідає останньому номеру помилки, поверненому [yaz\_errno()](function.yaz-errno.md)

### Список параметрів

`id`

Ресурс підключення, що повертається [yaz\_connect()](function.yaz-connect.md)

### Значення, що повертаються

Повертає текстове повідомлення про помилку для сервера (останній запит) з ідентифікатором `id`. Якщо остання операція пройшла успішно, повертається порожній рядок.

### Дивіться також

-   [yaz\_errno()](function.yaz-errno.md) \- Повертає номер помилки
-   [yaz\_addinfo()](function.yaz-addinfo.md) \- Повертає додаткову інформацію у разі виникнення помилки
