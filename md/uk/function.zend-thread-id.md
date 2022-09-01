---
navigation:
  - function.version-compare.html: « versioncompare
  - function.zend-version.html: zendversion »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: zendthreadід
---
# zendthreadід

(PHP 5, PHP 7, PHP 8)

zendthreadid — Повертає унікальний ідентифікатор поточного потоку виконання

### Опис

```methodsynopsis
zend_thread_id(): int
```

Ця функція повертає унікальний ідентифікатор потоку виконання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор потоку виконання як цілого числа.

### Приклади

**Приклад #1 Приклад використання **zendthreadid()****

```php
<?php
$thread_id = zend_thread_id();

echo 'Идентификатор текущего потока выполнения: ' . $thread_id;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Идентификатор текущего потока выполнения: 7864
```

### Примітки

> **Зауваження**
> 
> Ця функція доступна, тільки якщо PHP зібраний за допомогою Zend (Zend Thread Safety) і працює в режимі налагодження (`--enable-debug`
