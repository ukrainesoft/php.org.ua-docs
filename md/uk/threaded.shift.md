---
navigation:
  - threaded.run.md: '« Threaded::run'
  - threaded.synchronized.md: 'Threaded::synchronized »'
  - index.md: PHP Manual
  - class.threaded.md: Threaded
title: 'Threaded::shift'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Threaded::shift

(PECL pthreads >= 2.0.0)

Threaded::shift — Обробка

### Опис

```methodsynopsis
public Threaded::shift(): mixed
```

Переміщує елемент із таблиці властивостей об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент таблиці властивостей об'єкта.

### Приклади

**Приклад #1 Переміщення першого елемента таблиці властивостей пов'язаного об'єкта**

```php
<?php
$safe = new Threaded();

while (count($safe) < 10)
    $safe[] = count($safe);

var_dump($safe->shift());
?>
```

Результат виконання наведеного прикладу:

```
int(0)
```
