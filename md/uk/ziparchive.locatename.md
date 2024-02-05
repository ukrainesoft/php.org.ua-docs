---
navigation:
  - ziparchive.isencryptionmethoddupported.md: '« ZipArchive::isEncryptionMethodSupported'
  - ziparchive.open.md: 'ZipArchive::open »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::locateName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::locateName

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.5.0)

ZipArchive::locateName — Повертає індекс елемента в архіві

### Опис

```methodsynopsis
public ZipArchive::locateName(string $name, int $flags = 0): int|false
```

Знаходить елемент на його ім'я.

### Список параметрів

`name`

Назва елемента для пошуку.

`flags`

Прапори, що визначаються бітовою маскою з наступних значень, або 0 для жодного з них.

-   **`ZipArchive::FL_NOCASE`**
    
-   **`ZipArchive::FL_NODIR`**
    

### Значення, що повертаються

Повертає індекс елемента у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Створюється архів, а потім використовується метод **ZipArchive::locateName()****

```php
<?php
$file = 'testlocate.zip';

$zip = new ZipArchive;
if ($zip->open($file, ZipArchive::CREATE) !== TRUE) {
    exit('ошибка');
}

$zip->addFromString('entry1.txt', 'entry #1');
$zip->addFromString('entry2.txt', 'entry #2');
$zip->addFromString('dir/entry2d.txt', 'entry #2');

if ($zip->status !== ZipArchive::ER_OK) {
    echo "Ошибка записи в zip\n";
}
$zip->close();

if ($zip->open($file) !== TRUE) {
    exit('ошибка');
}

echo $zip->locateName('entry1.txt') . "\n";
echo $zip->locateName('eNtry2.txt') . "\n";
echo $zip->locateName('eNtry2.txt', ZipArchive::FL_NOCASE) . "\n";
echo $zip->locateName('enTRy2d.txt', ZipArchive::FL_NOCASE|ZipArchive::FL_NODIR) . "\n";
$zip->close();

?>
```

Результат виконання наведеного прикладу:

```
0

1
2
```
