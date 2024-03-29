---
navigation:
  - filters.md: « Список доступних фільтрів
  - filters.convert.md: Перетворювальні фільтри »
  - index.md: PHP Manual
  - filters.md: Список доступних фільтрів
title: Стрічкові фільтри
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Стрічкові фільтри

Всі ці фільтри служать для того самого, що мають на увазі їх імена відповідно до поведінки вбудованих в PHP функцій для роботи з рядками. Для отримання додаткової інформації про конкретний фільтр зверніться до сторінки посібника відповідної функції.

## string.rot13

Використання цього фільтра еквівалентно обробці всіх даних потоку функцією [str\_rot13()](function.str-rot13.md)

**Приклад #1 string.rot13**

```php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'string.rot13');
fwrite($fp, "This is a test.\n");
/* Выведет:  Guvf vf n grfg.   */
?>
```

## string.toupper

Використання цього фільтра еквівалентно обробці всіх даних потоку функцією [strtoupper()](function.strtoupper.md)

**Приклад #2 string.toupper**

```php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'string.toupper');
fwrite($fp, "This is a test.\n");
/* Выведет:  THIS IS A TEST.   */
?>
```

## string.tolower

Використання цього фільтра еквівалентно обробці всіх даних потоку функцією [strtolower()](function.strtolower.md)

**Приклад #3 string.tolower**

```php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'string.tolower');
fwrite($fp, "This is a test.\n");
/* Выведет:  this is a test.   */
?>
```

## string.strip\_tags

Використання цього фільтра еквівалентно обробці всіх даних потоку функцією [strip\_tags()](function.strip-tags.md). Він приймає аргументи в одній із двох форм: Або у вигляді рядка зі списком тегів, як і другий аргумент функції [strip\_tags()](function.strip-tags.md), чи масив назв тегів.

**Увага**

Ця функціональність оголошена *застарілої* починаючи з PHP 7.3.0 і її украй не рекомендується використовувати.

**Приклад #4 string.strip\_tags**

```php
<?php
$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'string.strip_tags', STREAM_FILTER_WRITE, "<b><i><u>");
fwrite($fp, "<b>bolded text</b> enlarged to a <h1>level 1 heading</h1>\n");
fclose($fp);
/* Выведет:  bolded text enlarged to a level 1 heading   */

$fp = fopen('php://output', 'w');
stream_filter_append($fp, 'string.strip_tags', STREAM_FILTER_WRITE, array('b','i','u'));
fwrite($fp, "<b>bolded text</b> enlarged to a <h1>level 1 heading</h1>\n");
fclose($fp);
/* Выведет:  bolded text enlarged to a level 1 heading   */
?>
```
