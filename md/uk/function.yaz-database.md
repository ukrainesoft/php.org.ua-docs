---
navigation:
  - function.yaz-connect.html: « yazconnect
  - function.yaz-element.html: yazelement »
  - index.html: PHP Manual
  - ref.yaz.html: Функции YAZ
title: yazdatabase
---
# yazdatabase

(PHP 4> = 4.0.6, PECL yaz> = 0.9.0)

yazdatabase — Визначає бази даних у сеансі

### Опис

```methodsynopsis
yaz_database(resource $id, string $databases): bool
```

Функція дозволяє змінювати бази даних протягом сеансу, вказавши одну або кілька баз даних, які будуть використовуватися для пошуку, пошуку і т.д. - перевизначення баз даних, вказаних у виклику [yazconnect()](function.yaz-connect.html)

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yazconnect()](function.yaz-connect.html)

`databases`

Рядок, що містить одну або кілька баз даних. Декілька баз даних, розділені знаком плюс `+`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
