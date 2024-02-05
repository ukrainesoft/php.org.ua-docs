---
navigation:
  - function.getdate.md: « getdate
  - function.gmdate.md: gmdate »
  - index.md: PHP Manual
  - ref.datetime.md: Функції дати та часу
title: gettimeofday
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gettimeofday

(PHP 4, PHP 5, PHP 7, PHP 8)

gettimeofday — Повертає поточний час

### Опис

```methodsynopsis
gettimeofday(bool $as_float = false): array|float
```

Функція є інтерфейсом до системного виклику gettimeofday(2). Вона повертає асоціативний масив, що містить інформацію, одержану від системного виклику.

### Список параметрів

`as_float`

Если установлено в\*\*`true`\*\*замість масиву повертається число з плаваючою точкою.

### Значення, що повертаються

По умолчанию возвращается массив (array). Если установлен параметр`as_float`, то повертається число з плаваючою точкою (float).

Ключі масиву:

-   "sec" - кількість секунд, що минули з епохи Unix
-   "usec" - мікросекунди
-   "minuteswest" - зсув на захід від Грінвіча, в хвилинах
-   "dsttime" - тип корекції літнього часу

### Приклади

**Пример #1 Пример использования функции**gettimeofday()\*\*\*\*

```php
<?php
print_r(gettimeofday());

echo gettimeofday(true);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [sec] => 1073504408
    [usec] => 238215
    [minuteswest] => 0
    [dsttime] => 1
)

1073504408.23910
```
