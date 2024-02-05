---
navigation:
  - function.zend-thread-id.md: « zend\_thread\_id
  - book.phpdbg.md: phpdbg »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: zend\_version
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zend\_version

(PHP 4, PHP 5, PHP 7, PHP 8)

zend\_version — Отримує версію двигуна Zend

### Опис

```methodsynopsis
zend_version(): string
```

Повертає рядок з номером версії ядра Zend Engine, що працює в даний момент.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає номер версії Zend Engine у ​​вигляді рядка.

### Приклади

**Пример #1 Пример использования**zend\_version()\*\*\*\*

```php
<?php
echo "Версия движка Zend: " . zend_version();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Версия движка Zend: 2.2.0
```

### Дивіться також

-   [phpinfo()](function.phpinfo.md) \- Виводить інформацію про поточну конфігурацію PHP
-   [phpcredits()](function.phpcredits.md) \- Виводить список розробників PHP
-   [phpversion()](function.phpversion.md) \- Отримує поточну версію PHP
