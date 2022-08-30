Повертає об'єкт елемента з RAR архіву

-   [« RarArchive::getEntries](rararchive.getentries.html)
    
-   [RarArchive::isBroken »](rararchive.isbroken.html)
    
-   [PHP Manual](index.html)
    
-   [RarArchive](class.rararchive.html)
    
-   Повертає об'єкт елемента з RAR архіву
    

# RarArchive::getEntry

# rarentryget

(PECL rar >= 2.0.0)

RarArchive::getEntry -- rarentryget — Повертає об'єкт елемента з RAR архіву

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public RarArchive::getEntry(string $entryname): RarEntry|false
```

Процедурний стиль:

```methodsynopsis
rar_entry_get(RarArchive $rarfile, string $entryname): RarEntry|false
```

Повертає об'єкт елемента (файл або директорію) з архіву RAR

> **Зауваження**
> 
> Ви також можете отримати об'єкти елементів за допомогою [RarArchive::getEntries()](rararchive.getentries.html)
> 
> Зверніть увагу, що RAR архів може мати кілька елементів з однаковим ім'ям. Цей метод поверне лише перший із них.

### Список параметрів

`rarfile`

Об'єкт [RarArchive](class.rararchive.html) відкритий за допомогою [raropen()](rararchive.open.html)

`entryname`

Дорога до елемента RAR архіву.

> **Зауваження**
> 
> Шлях повинен бути таким же, як і методом, що повертається. [RarEntry::getName()](rarentry.getname.html)

### Значення, що повертаються

Повертає знайдений об'єкт [RarEntry](class.rarentry.html) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$rar_arch = RarArchive::open('solid.rar');
if ($rar_arch === FALSE)
    die("Не смог открыть RAR архив.");
$rar_entry = $rar_arch->getEntry('tese.txt');
if ($rar_entry === FALSE)
    die("Не смог достать этот объект");
echo get_class($rar_entry)."\n";
echo $rar_entry;
$rar_arch->close();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
RarEntry
RarEntry for file "tese.txt" (23b93a7a)
```

**Приклад #2 Процедурний стиль**

```php
<?php
$rar_arch = rar_open('solid.rar');
if ($rar_arch === FALSE)
    die("Не смог открыть RAR архив.");
$rar_entry = rar_entry_get($rar_arch, 'tese.txt');
if ($rar_entry === FALSE)
    die("Не смог достать этот объект");
echo get_class($rar_entry)."\n";
echo $rar_entry;
rar_close($rar_arch);
?>
```

### Дивіться також

-   [RarArchive::getEntries()](rararchive.getentries.html) - Повертає повний список елементів із RAR архіву
-   [`rar://`обработчик (wrapper)](wrappers.rar.html)