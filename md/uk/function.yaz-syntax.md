---
navigation:
  - function.yaz-sort.md: « yaz\_sort
  - function.yaz-wait.md: yaz\_wait »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_syntax
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_syntax

(PHP 4 >= 4.0.1, PECL yaz >= 0.9.0)

yaz\_syntax — Вказує синтаксис, який ви бажаєте отримати для запису

### Опис

```methodsynopsis
yaz_syntax(resource $id, string $syntax): void
```

**yaz\_syntax()** задає синтаксис, що віддається перевагу, для видобутого запису

Функція має бути викликана до [yaz\_search()](function.yaz-search.md) або [yaz\_present()](function.yaz-present.md)

### Список параметрів

`id`

Дескриптор з'єднання, що повертається [yaz\_connect()](function.yaz-connect.md)

`syntax`

Синтаксис має бути заданий як OID (Object Identifier, ідентифікатор об'єкта) у вихідному форматі, розділеному точками (наприклад `1.2.840.10003.5.10`) або як відомий зареєстрований формат запису (sutrs, usmarc, grs1, xml та ін).

### Значення, що повертаються

Функція не повертає значення після виконання.
