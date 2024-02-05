---
navigation:
  - phar.mungserver.md: '« Phar::mungServer'
  - phar.offsetget.md: 'Phar::offsetGet »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::offsetExists'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::offsetExists

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::offsetExists — Визначити, чи є файл в архіві

### Опис

```methodsynopsis
public Phar::offsetExists(string $localName): bool
```

Це реалізація інтерфейсу [ArrayAccess](class.arrayaccess.md)дозволяє маніпулювати вмістом Phar-архіву в стилі доступу до елементів масиву.

offsetExists() запускається щоразу, коли викликається [isset()](function.isset.md)

### Список параметрів

`localName`

Ім'я файлу (відносний шлях).

### Значення, що повертаються

Повертає **`true`**, якщо файл присутній в архіві та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** Phar::offsetExists()\*\*\*\*

```php
<?php
$p = new Phar(dirname(__FILE__) . '/my.phar', 0, 'my.phar');
$p['firstfile.txt'] = 'первый файл';
$p['secondfile.txt'] = 'второй файл';
// в следующих строках offsetExists() вызывается косвенно
var_dump(isset($p['firstfile.txt']));
var_dump(isset($p['nothere.txt']));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [Phar::offsetGet()](phar.offsetget.md) \- Отримати PharFileInfo об'єкт для конкретного файлу
-   [Phar::offsetSet()](phar.offsetset.md) \- Зміна вмісту файлу
-   [Phar::offsetUnset()](phar.offsetunset.md) \- Видалити файл із phar-архіву
