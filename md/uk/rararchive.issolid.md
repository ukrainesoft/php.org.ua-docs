---
navigation:
  - rararchive.isbroken.md: '« RarArchive::isBroken'
  - rararchive.open.md: 'RarArchive::open »'
  - index.md: PHP Manual
  - class.rararchive.md: RarArchive
title: 'RarArchive::isSolid'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarArchive::isSolid

# rar\_solid\_is

(PECL rar >= 2.0.0)

RarArchive::isSolid -- rar\_solid\_is — Перевірити, чи є архів суцільним

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

Об'єкт [RarArchive](class.rararchive.md), відкритий за допомогою [rar\_open()](rararchive.open.md)

### Значення, що повертаються

Повертає **`true`**, если да и\*\*`false`\*\*, якщо ні.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$arch1 = RarArchive::open("store_method.rar");
$arch2 = RarArchive::open("solid.rar");
echo "$arch1: " . ($arch1->isSolid()?'yes':'no') ."\n";
echo "$arch2: " . ($arch2->isSolid()?'yes':'no') . "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
RAR Archive "C:\php_rar\trunk\tests\store_method.rar": no
RAR Archive "C:\php_rar\trunk\tests\solid.rar": yes
```

**Приклад #2 Процедурний стиль**

```php
<?php
$arch1 = rar_open("store_method.rar");
$arch2 = rar_open("solid.rar");
echo "$arch1: " . (rar_solid_is($arch1)?'yes':'no') ."\n";
echo "$arch2: " . (rar_solid_is($arch2)?'yes':'no') . "\n";
?>
```
