---
navigation:
  - function.yaz-element.md: « yazelement
  - function.yaz-error.md: yazerror »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazerrno
---
# yazerrno

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazerrno — Повертає номер помилки

### Опис

```methodsynopsis
yaz_errno(resource $id): int
```

Повертає номер помилки для сервера (останній запит) з ідентифікатором `id`

**yazerrno()** повинен викликатись після мережної активності для кожного сервера (після повернення [yazwait()](function.yaz-wait.md)), щоб визначити успішне виконання або помилку останньої операції (наприклад, пошуку).

### Список параметрів

`id`

Ресурс підключення, що повертається [yazconnect()](function.yaz-connect.md)

### Значення, що повертаються

Повертає код помилки. Код помилки - це діагностичний код Z39.50 (зазвичай діагностика Bib-1), або код помилки на стороні клієнта, який генерується самим PHP/YAZ, наприклад "Connect failed", "Init Rejected" і т.д.

### Дивіться також

-   [yazerror()](function.yaz-error.md) - Повертає опис помилки
-   [yazaddinfo()](function.yaz-addinfo.md) - Повертає додаткову інформацію у разі виникнення помилки
