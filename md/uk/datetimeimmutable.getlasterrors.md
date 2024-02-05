---
navigation:
  - datetimeimmutable.createfrommutable.md: '« DateTimeImmutable::createFromMutable'
  - datetimeimmutable.modify.md: 'DateTimeImmutable::modify »'
  - index.md: PHP Manual
  - class.datetimeimmutable.md: DateTimeImmutable
title: 'DateTimeImmutable::getLastErrors'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DateTimeImmutable::getLastErrors

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

DateTimeImmutable::getLastErrors — Повертає попередження та помилки

### Опис

```methodsynopsis
public static DateTimeImmutable::getLastErrors(): array|false
```

Повертає масив, що містить повідомлення про помилки та попередження, виявлені при розборі рядка дати/часу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить інформацію про попередження та помилки або \*\*`false`\*\*якщо немає ні попереджень, ні помилок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | До версії PHP 8.2.0 функція не повертала \*\*`false`\*\*якщо не було попереджень або помилок. Натомість вона завжди повертала задокументовану структуру масиву. |

### Приклади

**Приклад #1 Приклад використання** DateTimeImmutable::getLastErrors()\*\*\*\*

```php
<?php
try {
    $date = new DateTimeImmutable('asdfasdf');
} catch (Exception $e) {
    // Только в целях демонстрации...
    print_r(DateTimeImmutable::getLastErrors());

    // в объектно-ориентированном стиле лучше делать так:
    // echo $e->getMessage();
}
?>
```

Результат виконання наведених прикладів:

```
Array
(
   [warning_count] => 1
   [warnings] => Array
       (
           [6] => Double timezone specification
       )

   [error_count] => 1
   [errors] => Array
       (
           [0] => The timezone could not be found in the database
       )

)
```

Індекси 6 та 0 вказують на символьні позиції у рядку, де сталася помилка.
