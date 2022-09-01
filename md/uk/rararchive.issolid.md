---
navigation:
  - rararchive.isbroken.html: '« RarArchive::isBroken'
  - rararchive.open.html: 'RarArchive::open »'
  - index.html: PHP Manual
  - class.rararchive.html: RarArchive
title: 'RarArchive::isSolid'
---
# RarArchive::isSolid

# rarsolidіс

(PECL rar >= 2.0.0)

RarArchive::isSolid -- rarsolidis — Перевірити, чи є архів суцільним

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public RarArchive::isSolid(): bool
```

Процедурний стиль:

```methodsynopsis
rar_solid_is(RarArchive $rarfile): bool
```

Перевіряє, чи є архів суцільним. Вилучення одного конкретного файлу з суцільного архіву помітно повільніше.

### Список параметрів

`rarfile`

Об'єкт [RarArchive](class.rararchive.html), відкритий за допомогою [raropen()](rararchive.open.html)

### Значення, що повертаються

Повертає **`true`**, якщо так і **`false`**, якщо ні.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$arch1 = RarArchive::open("store_method.rar");
$arch2 = RarArchive::open("solid.rar");
echo "$arch1: " . ($arch1->isSolid()?'yes':'no') ."\n";
echo "$arch2: " . ($arch2->isSolid()?'yes':'no') . "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
RAR Archive "C:\php_rar\trunk\tests\store_method.rar": no
RAR Archive "C:\php_rar\trunk\tests\solid.rar": yes
```

**Приклад #2 Процедурний стиль**

```php
<?php
$arch1 = rar_open("store_method.rar");
$arch2 = rar_open("solid.rar");
echo "$arch1: " . (rar_solid_is($arch1)?'yes':'no') ."\n";
echo "$arch2: " . (rar_solid_is($arch2)?'yes':'no') . "\n";
?>
```
