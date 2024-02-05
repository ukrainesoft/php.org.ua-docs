---
navigation:
  - rararchive.getcomment.md: '« RarArchive::getComment'
  - rararchive.getentry.md: 'RarArchive::getEntry »'
  - index.md: PHP Manual
  - class.rararchive.md: RarArchive
title: 'RarArchive::getEntries'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarArchive::getEntries

# rar\_list

(PECL rar >= 2.0.0)

RarArchive::getEntries -- rar\_list — Повертає повний список елементів із RAR архіву

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

> **Зауваження** :
> 
> Якщо архів має елементи з однаковим ім'ям, цей метод спільно з циклом `foreach`по[RarArchive](class.rararchive.md) і доступом до нього як масиву з числовими індексами є єдиними способами отримати доступ до цих елементів (тобто . [RarArchive::getEntry()](rararchive.getentry.md) і [`rar://`обработчик (wrapper)](wrappers.rar.md)не помогут).

### Список параметрів

`rarfile`

Об'єкт [RarArchive](class.rararchive.md) відкритий за допомогою [rar\_open()](rararchive.open.md)

### Значення, що повертаються

**rar\_list()** повертає масив об'єктів [RarEntry](class.rarentry.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL rar 3.0.0 | Виправлена ​​підтримка RAR архівів з іменами елементів, що повторюються. |

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
$rar_arch = RarArchive::open('solid.rar');
if ($rar_arch === FALSE)
    die("Не смог открыть RAR архив.");

$rar_entries = $rar_arch->getEntries();
if ($rar_entries === FALSE)
    die("Не смог достать содержимое.");

echo "Нашёл " . count($rar_entries) . " объектов.\n";

foreach ($rar_entries as $e) {
    echo $e;
    echo "\n";
}
$rar_arch->close();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Нашёл 2 объектов.
RarEntry for file "tese.txt" (23b93a7a)
RarEntry for file "unrardll.txt" (2ed64b6e)
```

**Приклад #2 Процедурний стиль**

```php
<?php
$rar_arch = rar_open('solid.rar');
if ($rar_arch === FALSE)
    die("Could not open RAR archive.");

$rar_entries = rar_list($rar_arch);
if ($rar_entries === FALSE)
    die("Could retrieve entries.");

echo "Found " . count($rar_entries) . " entries.\n";

foreach ($rar_entries as $e) {
    echo $e;
    echo "\n";
}
rar_close($rar_arch);
?>
```

### Дивіться також

-   [RarArchive::getEntry()](rararchive.getentry.md) \- Повертає об'єкт елемента з архіву RAR
-   [`rar://`обробник(wrapper)](wrappers.rar.md)
