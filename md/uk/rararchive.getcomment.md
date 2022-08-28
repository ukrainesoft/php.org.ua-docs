Отримати текст коментаря з архіву RAR

-   [« RarArchive::close](rararchive.close.html)
    
-   [RarArchive::getEntries »](rararchive.getentries.html)
    
-   [PHP Manual](index.html)
    
-   [RarArchive](class.rararchive.html)
    
-   Отримати текст коментаря з архіву RAR
    

# RarArchive::getComment

# rarcommentget

(PECL rar >= 2.0.0)

RarArchive::getComment -- rarcommentget — Отримати текст коментаря з архіву RAR

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

> **Зауваження**
> 
> Модуль не підтримує коментарів на рівні записів.

### Список параметрів

`rarfile`

Об'єкт [RarArchive](class.rararchive.html), відкритий за допомогою [rar\_open()](rararchive.open.html)

### Значення, що повертаються

Повертає коментар або **`null`**якщо його немає.

> **Зауваження**
> 
> RAR зараз не підтримує коментарі в unicode. Кодування результату не визначено, але, можливо, воно буде Windows-1252.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$rar_arch = RarArchive::open('commented.rar');
echo $rar_arch->getComment();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
This is the comment of the file commented.rar.
```

**Приклад #2 Процедурний стиль**

```php
<?php
$rar_arch = rar_open('commented.rar');
echo rar_comment_get($rar_arch);
?>
```