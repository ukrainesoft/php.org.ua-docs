Повертає повний список елементів із RAR архіву

-   [« RarArchive::getComment](rararchive.getcomment.html)
    
-   [RarArchive::getEntry »](rararchive.getentry.html)
    
-   [PHP Manual](index.html)
    
-   [RarArchive](class.rararchive.html)
    
-   Повертає повний список елементів із RAR архіву
    

# RarArchive::getEntries

# rarlist

(PECL rar >= 2.0.0)

RarArchive::getEntries -- rarlist — Повертає повний список елементів із RAR архіву

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public RarArchive::getEntries(): array|false
```

Процедурний стиль:

```methodsynopsis
rar_list(RarArchive $rarfile): array|false
```

Повертає елементи (файли та директорії) з RAR архіву.

> **Зауваження**
> 
> Якщо архів має елементи з однаковим ім'ям, цей метод спільно з циклом `foreach` по [RarArchive](class.rararchive.html) і доступом до нього як масиву з числовими індексами є єдиними способами отримати доступ до цих елементів (тобто . [RarArchive::getEntry()](rararchive.getentry.html) і [`rar://`обработчик (wrapper)](wrappers.rar.html) не допоможуть).

### Список параметрів

`rarfile`

Об'єкт [RarArchive](class.rararchive.html) відкритий за допомогою [raropen()](rararchive.open.html)

### Значення, що повертаються

**rarlist()** повертає масив об'єктів [RarEntry](class.rarentry.html) або **`false`** у разі виникнення помилки.

### список змін

| Версия         | Описание                                                                 |
|----------------|--------------------------------------------------------------------------|
| PECL rar 3.0.0 | Виправлена ​​підтримка RAR архівів з іменами елементів, що повторюються. |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$rar_arch = RarArchive::open('solid.rar');
if ($rar_arch === FALSE)
    die("Не смог открыть RAR архив.");

$rar_entries = $rar_arch->getEntries();
if ($rar_entries === FALSE)
    die("Не смог достать содержимое.");

echo "Нашёл " . count($rar_entries) . " объектов.\n";

foreach ($rar_entries as $e) {
    echo $e;
    echo "\n";
}
$rar_arch->close();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Нашёл 2 объектов.
RarEntry for file "tese.txt" (23b93a7a)
RarEntry for file "unrardll.txt" (2ed64b6e)
```

**Приклад #2 Процедурний стиль**

```php
<?php
$rar_arch = rar_open('solid.rar');
if ($rar_arch === FALSE)
    die("Could not open RAR archive.");

$rar_entries = rar_list($rar_arch);
if ($rar_entries === FALSE)
    die("Could retrieve entries.");

echo "Found " . count($rar_entries) . " entries.\n";

foreach ($rar_entries as $e) {
    echo $e;
    echo "\n";
}
rar_close($rar_arch);
?>
```

### Дивіться також

-   [RarArchive::getEntry()](rararchive.getentry.html) - Повертає об'єкт елемента з архіву RAR
-   [`rar://`обработчик(wrapper)](wrappers.rar.html)