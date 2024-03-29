---
navigation:
  - rararchive.close.md: '« RarArchive::close'
  - rararchive.getentries.md: 'RarArchive::getEntries »'
  - index.md: PHP Manual
  - class.rararchive.md: RarArchive
title: 'RarArchive::getComment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarArchive::getComment

# rar\_comment\_get

(PECL rar >= 2.0.0)

RarArchive::getComment -- rar\_comment\_get — Отримати текст коментаря з архіву RAR

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public RarArchive::getComment(): string
```

Процедурний стиль:

```methodsynopsis
rar_comment_get(RarArchive $rarfile): string
```

Повертає (глобальний) коментар, збережений в архіві RAR. Він може бути довжиною до 64 KiB.

> **Зауваження** :
> 
> Модуль не підтримує коментарів на рівні записів.

### Список параметрів

`rarfile`

Об'єкт [RarArchive](class.rararchive.md), відкритий за допомогою [rar\_open()](rararchive.open.md)

### Значення, що повертаються

Повертає коментар або \*\*`null`\*\*якщо його немає.

> **Зауваження** :
> 
> RAR зараз не підтримує коментарі в unicode. Кодування результату не визначено, але, можливо, воно буде Windows-1252.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$rar_arch = RarArchive::open('commented.rar');
echo $rar_arch->getComment();
?>
```

Висновок наведеного прикладу буде схожим на:

```
This is the comment of the file commented.rar.
```

**Приклад #2 Процедурний стиль**

```php
<?php
$rar_arch = rar_open('commented.rar');
echo rar_comment_get($rar_arch);
?>
```
