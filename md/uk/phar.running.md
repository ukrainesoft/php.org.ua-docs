---
navigation:
  - phar.offsetunset.md: '« Phar::offsetUnset'
  - phar.setalias.md: 'Phar::setAlias »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::running'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::running

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::running — Отримати повний шлях на диску або повний URL запущеного Phar-архіву

### Опис

```methodsynopsis
final public static Phar::running(bool $returnPhar = true): string
```

Повертає повний шлях запущеного архіву. Використовується для того ж, для чого використовується константа `__FILE__` і працює лише всередині запущеного phar-архіву.

При запуске**Phar::running()**из загрузчика результат будет`""`Внутри загрузчика используйте константу**`__FILE__`**

### Список параметрів

`returnPhar`

Якщо **`false`**, буде повернуто повний дисковий шлях до phar-архіву. Якщо **`true`**, то буде повернено повну URL-адресу.

### Значення, що повертаються

Поверне шлях, якщо він коректний, або порожній рядок.

### Приклади

**Приклад #1 Приклад використання** Phar::running()\*\*\*\*

Для следующего Приклада предположим, что архив находится по пути`/path/to/phar/my.phar`

```php
<?php
$a = Phar::running(); // $a равно "phar:///path/to/my.phar"
$b = Phar::running(false); // $b равно "/path/to/my.phar"
?>
```
