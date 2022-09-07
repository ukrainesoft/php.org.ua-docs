---
navigation:
  - phar.getsignature.md: '« Phar::getSignature'
  - phar.getsupportedcompression.md: 'Phar::getSupportedCompression »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::getStub'
---
# Phar::getStub

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::getStub — Отримати завантажувач PHP або завантажувач заглушки Phar-архіву

### Опис

```methodsynopsis
public Phar::getStub(): string
```

Phar-архіви містять початкове завантаження або заглушку (`stub`), написану на PHP, який запускається при запуску архіву, коли його підключають через include:

```php
<?php
include 'myphar.phar';
?>
```

або просто запускають:

```
php myphar.phar
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок із вмістом початкового завантажувача (заглушки) поточного Phar-архіву.

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо з будь-яких причин не може отримати текст завантажувача.

### Приклади

**Приклад #1 Приклад використання **Phar::getStub()****

```php
<?php
$p = new Phar('/path/to/my.phar', 0, 'my.phar');
echo $p->getStub();
echo "==NEXT==\n";
$p->setStub("<?php
function __autoload($class)
{
    include 'phar://' . str_replace('_', '/', $class);
}
Phar::mapPhar('myphar.phar');
include 'phar://myphar.phar/startup.php';
__HALT_COMPILER(); ?>");
echo $p->getStub();
?>
```

Результат виконання цього прикладу:

```
<?php __HALT_COMPILER(); ?>
==NEXT==
<?php
function __autoload($class)
{
    include 'phar://' . str_replace('_', '/', $class);
}
Phar::mapPhar('myphar.phar');
include 'phar://myphar.phar/startup.php';
__HALT_COMPILER(); ?>
```

### Дивіться також

-   [Phar::setStub()](phar.setstub.md) - Встановити завантажувач або завантажувальну заглушку в Phar-архів
-   [Phar::createDefaultStub()](phar.createdefaultstub.md) - Створити заглушку у форматі phar-архіву
