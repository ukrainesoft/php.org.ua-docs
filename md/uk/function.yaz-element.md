---
navigation:
  - function.yaz-database.md: « yaz\_database
  - function.yaz-errno.md: yaz\_errno »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_element
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_element

(PHP 4 >= 4.0.1, PECL yaz >= 0.9.0)

yaz\_element — Вказує ім'я набору елементів для пошуку

### Опис

```methodsynopsis
yaz_element(resource $id, string $elementset): bool
```

Функція встановлює ім'я набору елементів пошуку.

Викличте цю функцію перед [yaz\_search()](function.yaz-search.md) або [yaz\_present()](function.yaz-present.md), щоб вказати ім'я набору елементів для записів, що виймаються.

> **Зауваження** :
> 
> Якщо здається, що не відбувається жодного ефекту, дивіться опис опції `piggybacking`в[yaz\_connect()](function.yaz-connect.md)

### Список параметрів

`id`

Ресурс з'єднання, повернутий [yaz\_connect()](function.yaz-connect.md)

`elementset`

Більшість серверів підтримують `F` (для повних записів) та `B`(для кратких записей).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
