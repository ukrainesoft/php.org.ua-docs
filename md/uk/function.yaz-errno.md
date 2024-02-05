---
navigation:
  - function.yaz-element.md: « yaz\_element
  - function.yaz-error.md: yaz\_error »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_errno
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_errno

(PHP 4 >= 4.0.1, PECL yaz >= 0.9.0)

yaz\_errno — Повертає номер помилки

### Опис

```methodsynopsis
yaz_errno(resource $id): int
```

Повертає номер помилки для сервера (останній запит) з ідентифікатором `id`

**yaz\_errno()** повинен викликатись після мережної активності для кожного сервера (після повернення [yaz\_wait()](function.yaz-wait.md)), щоб визначити успішне виконання або помилку останньої операції (наприклад, пошуку).

### Список параметрів

`id`

Ресурс підключення, що повертається [yaz\_connect()](function.yaz-connect.md)

### Значення, що повертаються

Повертає код помилки. Код помилки - це діагностичний код Z39.50 (зазвичай діагностика Bib-1), або код помилки на стороні клієнта, який генерується самим PHP/YAZ, наприклад "Connect failed", "Init Rejected" і т.д.

### Дивіться також

-   [yaz\_error()](function.yaz-error.md) \- Повертає опис помилки
-   [yaz\_addinfo()](function.yaz-addinfo.md) \- Повертає додаткову інформацію у разі виникнення помилки
