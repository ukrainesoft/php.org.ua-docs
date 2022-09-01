---
navigation:
  - function.yaz-sort.html: « yazsort
  - function.yaz-wait.html: yazwait »
  - index.md: PHP Manual
  - ref.yaz.md: Функции YAZ
title: yazsyntax
---
# yazsyntax

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazsyntax — Вказує синтаксис, який ви бажаєте отримати для запису

### Опис

```methodsynopsis
yaz_syntax(resource $id, string $syntax): void
```

**yazsyntax()** задає синтаксис, що віддається перевагу, для видобутого запису

Функція повинна бути викликана до [yazsearch()](function.yaz-search.html) або [yazpresent()](function.yaz-present.html)

### Список параметрів

`id`

Дескриптор з'єднання, що повертається [yazconnect()](function.yaz-connect.html)

`syntax`

Синтаксис має бути заданий як OID (Object Identifier, ідентифікатор об'єкта) у вихідному форматі, розділеному точками (наприклад `1.2.840.10003.5.10`) або як відомий зареєстрований формат запису (sutrs, usmarc, grs1, xml та ін).

### Значення, що повертаються

Функція не повертає значення після виконання.
