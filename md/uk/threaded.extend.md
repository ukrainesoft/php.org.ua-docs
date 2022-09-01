---
navigation:
  - threaded.count.md: '« Threaded::count'
  - thread.isrunning.md: 'Threaded::isRunning »'
  - index.md: PHP Manual
  - class.threaded.md: Threaded
title: 'Threaded::extend'
---
# Threaded::extend

(PECL pthreads >= 2.0.8)

Threaded::extend — Обробка під час виконання

### Опис

```methodsynopsis
public Threaded::extend(string $class): bool
```

Робить потокобезпечний стандартний клас під час виконання.

### Список параметрів

`class`

Клас розширення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Спадкування під час виконання**

```php
<?php
class My {}

Threaded::extend(My::class);

$my = new My();

var_dump($my instanceof Threaded);
?>
```

Результат виконання цього прикладу:

```
bool(true)
```
