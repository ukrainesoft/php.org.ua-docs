---
navigation:
  - function.yaz-connect.md: « yaz\_connect
  - function.yaz-element.md: yaz\_element »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_database
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_database

(PHP 4 >= 4.0.6, PECL yaz >= 0.9.0)

yaz\_database — Визначає бази даних у сеансі

### Опис

```methodsynopsis
yaz_database(resource $id, string $databases): bool
```

Функція дозволяє змінювати бази даних протягом сеансу, вказавши одну або кілька баз даних, які будуть використовуватися для пошуку, пошуку і т.д. - перевизначення баз даних, вказаних у виклику [yaz\_connect()](function.yaz-connect.md)

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yaz\_connect()](function.yaz-connect.md)

`databases`

Рядок, що містить одну або кілька баз даних. Декілька баз даних, розділені знаком плюс `+`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
