---
navigation:
  - function.version-compare.md: « version\_compare
  - function.zend-version.md: zend\_version »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: zend\_thread\_id
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zend\_thread\_id

(PHP 5, PHP 7, PHP 8)

zend\_thread\_id — Повертає унікальний ідентифікатор поточного потоку виконання

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

**Приклад #1 Приклад використання** zend\_thread\_id()\*\*\*\*

```php
<?php
$thread_id = zend_thread_id();

echo 'Идентификатор текущего потока выполнения: ' . $thread_id;
?>
```

Висновок наведеного прикладу буде схожим на:

```
Идентификатор текущего потока выполнения: 7864
```

### Примітки

> **Зауваження** :
> 
> Ця функція доступна, тільки якщо PHP зібраний за допомогою Zend (Zend Thread Safety) і працює в режимі налагодження (`--enable-debug`
