---
navigation:
  - rararchive.getentry.md: '« RarArchive::getEntry'
  - rararchive.issolid.md: 'RarArchive::isSolid »'
  - index.md: PHP Manual
  - class.rararchive.md: RarArchive
title: 'RarArchive::isBroken'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarArchive::isBroken

# rar\_broken\_is

(PECL rar >= 3.0.0)

RarArchive::isBroken -- rar\_broken\_is — Перевіряє, чи не зламано архів (не завершено)

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public RarArchive::isBroken(): bool
```

Процедурний стиль:

```methodsynopsis
rar_broken_is(RarArchive $rarfile): bool
```

Функція визначає, чи є архів незавершеним, тобто. том обрізаний чи відсутній.

### Список параметрів

`rarfile`

Об'єкт [RarArchive](class.rararchive.md), відкритий за допомогою [rar\_open()](rararchive.open.md)

### Значення, що повертаються

Повертає **`true`**, якщо архів зламаний і **`false`**, якщо ні. Також, функція може повернути **`false`**, якщо надісланий файл вже закрито. Єдиний варіант визначити точну причину – це дозволити винятки за допомогою [RarException::setUsingExceptions()](rarexception.setusingexceptions.md); однак, це не так вже й важливо, оскільки програма все одно не зможе працювати із закритим файлом.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
function retnull() { return null; }
$file = dirname(__FILE__) . "/multi_broken.part1.rar";
/* третий аргумент служит для подавления сообщений */
$arch = RarArchive::open($file, null, 'retnull');
var_dump($arch->isBroken());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
```

**Приклад #2 Процедурний стиль**

```php
<?php
function retnull() { return null; }
$file = dirname(__FILE__) . "/multi_broken.part1.rar";
/* третий аргумент служит для подавления сообщений */
$arch = rar_open($file, null, 'retnull');
var_dump(rar_broken_is($arch));
?>
```

### Дивіться також

-   [RarArchive::setAllowBroken()](rararchive.setallowbroken.md) \- Чи відкривати пошкоджені архіви
