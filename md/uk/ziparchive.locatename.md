Повертає індекс елемента у архіві

-   [« ZipArchive::isEncryptionMethodSupported](ziparchive.isencryptionmethoddupported.html)
    
-   [ZipArchive::open »](ziparchive.open.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Повертає індекс елемента у архіві
    

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

Повертає індекс елемента у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Створюється архів, а потім використовується метод **ZipArchive::locateName()****

```php
<?php
$file = 'testlocate.zip';

$zip = new ZipArchive;
if ($zip->open($file, ZipArchive::CREATE) !== TRUE) {
    exit('ошибка');
}

$zip->addFromString('entry1.txt', 'entry #1');
$zip->addFromString('entry2.txt', 'entry #2');
$zip->addFromString('dir/entry2d.txt', 'entry #2');

if ($zip->status !== ZipArchive::ER_OK) {
    echo "Ошибка записи в zip\n";
}
$zip->close();

if ($zip->open($file) !== TRUE) {
    exit('ошибка');
}

echo $zip->locateName('entry1.txt') . "\n";
echo $zip->locateName('eNtry2.txt') . "\n";
echo $zip->locateName('eNtry2.txt', ZipArchive::FL_NOCASE) . "\n";
echo $zip->locateName('enTRy2d.txt', ZipArchive::FL_NOCASE|ZipArchive::FL_NODIR) . "\n";
$zip->close();

?>
```

Результат виконання цього прикладу:

```
0

1
2
```