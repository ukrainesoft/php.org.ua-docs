---
navigation:
  - threaded.notifyone.html: '« Threaded::notifyOne'
  - threaded.run.html: 'Threaded::run »'
  - index.html: PHP Manual
  - class.threaded.html: Threaded
title: 'Threaded::pop'
---
# Threaded::pop

(PECL pthreads >= 2.0.0)

Threaded::pop — Обробка

### Опис

```methodsynopsis
public Threaded::pop(): bool
```

Витягує елемент із таблиці властивостей об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент таблиці властивостей об'єктів.

### Приклади

**Приклад #1 Вилучення останнього елемента з таблиці властивостей пов'язаного об'єкта**

```php
<?php
$safe = new Threaded();

while (count($safe) < 10)
    $safe[] = count($safe);

var_dump($safe->pop());
?>
```

Результат виконання цього прикладу:

```
int(9)
```
