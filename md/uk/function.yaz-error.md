---
navigation:
  - function.yaz-errno.md: « yazerrno
  - function.yaz-es-result.md: yazесresult »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazerror
---
# yazerror

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazerror — Повертає опис помилки

### Опис

```methodsynopsis
yaz_error(resource $id): string
```

**yazerror()** повертає текстове повідомлення англійською мовою, що відповідає останньому номеру помилки, поверненому [yazerrno()](function.yaz-errno.md)

### Список параметрів

`id`

Ресурс підключення, що повертається [yazconnect()](function.yaz-connect.md)

### Значення, що повертаються

Повертає текстове повідомлення про помилку для сервера (останній запит) з ідентифікатором `id`. Якщо остання операція пройшла успішно, повертається порожній рядок.

### Дивіться також

-   [yazerrno()](function.yaz-errno.md) - Повертає номер помилки
-   [yazaddinfo()](function.yaz-addinfo.md) - Повертає додаткову інформацію у разі виникнення помилки
