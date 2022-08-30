Читає рядок з файлу та видаляє HTML-теги

-   [« fgets](function.fgets.html)
    
-   [fileexists »](function.file-exists.html)
    
-   [PHP Manual](index.html)
    
-   [Функції файлової системи](ref.filesystem.html)
    
-   Читає рядок з файлу та видаляє HTML-теги
    

# fgetss

(PHP 4, PHP 5, PHP 7)

fgetss — Читає рядок із файлу та видаляє HTML-теги

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.3.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
fgetss(resource $handle, int $length = ?, string $allowable_tags = ?): string
```

Функція ідентична функції [fgets()](function.fgets.html), за винятком того, що **fgetss()** видаляє будь-які NULL-байти, HTML- та PHP-теги з прочитаного рядка. Функція зберігає стан синтаксичного аналізу від виклику до виклику і тому не еквівалентна виклику [striptags()](function.strip-tags.html) для значення, що повертається [fgets()](function.fgets.html)

### Список параметрів

`handle`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.html) або [fsockopen()](function.fsockopen.html) (і все ще не закритий функцією [fclose()](function.fclose.html)

`length`

Довжина даних.

`allowable_tags`

Можна використовувати третій необов'язковий параметр, щоб вказати теги, які не потрібно вирізати. Дивіться опис [striptags()](function.strip-tags.html) для більш детальної інформації про `allowable_tags`

### Значення, що повертаються

Повертає рядок завдовжки до `length` - 1 байт, прочитаних із файлу, на який вказує дескриптор `handle`, з вирізаними тегами HTML та PHP.

У разі виникнення помилки повертає **`false`**

### Приклади

**Приклад #1 Порядкове читання PHP-файлу**

```php
<?php
$str = <<<EOD
<html><body>
 <p>Добро пожаловать! Сегодня <?php echo(date('jS F')); ?>.</p>
</body></html>
Текст вне HTML-блока.
EOD;
file_put_contents('sample.php', $str);

$handle = @fopen("sample.php", "r");
if ($handle) {
    while (!feof($handle)) {
        $buffer = fgetss($handle, 4096);
        echo $buffer;
    }
    fclose($handle);
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Добро пожаловать! Сегодня .

Текст вне HTML-блока.
```

### Примітки

> **Зауваження**: Якщо у вас виникають проблеми з розпізнаванням PHP кінців рядків під час читання або створення файлів на Macintosh-сумісному комп'ютері, увімкнення опції [autodetectlineendings](filesystem.configuration.html#ini.auto-detect-line-endings) може допомогти вирішити проблему.

### Дивіться також

-   [fgets()](function.fgets.html) - Читає рядок із файлу
-   [fopen()](function.fopen.html) - Відкриває файл або URL
-   [popen()](function.popen.html) - Відкриває файловий покажчик процесу
-   [fsockopen()](function.fsockopen.html) - Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [striptags()](function.strip-tags.html) - Видаляє теги HTML та PHP з рядка
-   [SplFileObject::fgetss()](splfileobject.fgetss.html) - Отримати рядок із файлу та видалити теги HTML
-   Фільтр [string.striptags](filters.string.html#filters.string.strip_tags)