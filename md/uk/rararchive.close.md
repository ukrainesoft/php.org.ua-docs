---
navigation:
  - class.rararchive.md: « RarArchive
  - rararchive.getcomment.md: 'RarArchive::getComment »'
  - index.md: PHP Manual
  - class.rararchive.md: RarArchive
title: 'RarArchive::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarArchive::close

# rar\_close

(PECL rar >= 2.0.0)

RarArchive::close -- rar\_close — Закриває RAR архів та звільняє всі ресурси

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public RarArchive::close(): bool
```

Процедурний стиль:

```methodsynopsis
rar_close(RarArchive $rarfile): bool
```

Закриває RAR архів та звільняє всі ресурси, пов'язані з ним.

### Список параметрів

`rarfile`

Об'єкт [RarArchive](class.rararchive.md), відкритий за допомогою [rar\_open()](rararchive.open.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL rar 2.0.0 | Елементи архіву, що повертаються [RarArchive::getEntry()](rararchive.getentry.md) і [RarArchive::getEntries()](rararchive.getentries.md) тепер недійсні після виклику цього методу. Це означає, що немає гарантії правильної роботи всіх методів цих елементів. |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$rar_arch = RarArchive::open('latest_winrar.rar');
echo $rar_arch."\n";
$rar_arch->close();
echo $rar_arch."\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar"
RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar" (closed)
```

**Приклад #2 Процедурний стиль**

```php
<?php
$rar_arch = rar_open('latest_winrar.rar');
echo $rar_arch."\n";
rar_close($rar_arch);
echo $rar_arch."\n";
?>
```
