---
navigation:
  - function.fgets.md: « fgets
  - function.file-exists.md: file\_exists »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: fgetss
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fgetss

(PHP 4, PHP 5, PHP 7)

fgetss — Читає рядок із файлу та видаляє HTML-теги

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.3.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
fgetss(resource $handle, int $length = ?, string $allowable_tags = ?): string
```

Функція ідентична функції [fgets()](function.fgets.md), за винятком того, що **fgetss()** видаляє будь-які NULL-байти, HTML- та PHP-теги з прочитаного рядка. Функція зберігає стан синтаксичного аналізу від виклику до виклику і тому не еквівалентна виклику [strip\_tags()](function.strip-tags.md) для значення, що повертається [fgets()](function.fgets.md)

### Список параметрів

`handle`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.md) або [fsockopen()](function.fsockopen.md) (і все ще не закритий функцією [fclose()](function.fclose.md)

`length`

Довжина даних.

`allowable_tags`

Можна використовувати третій необов'язковий параметр, щоб вказати теги, які не потрібно вирізати. Дивіться опис [strip\_tags()](function.strip-tags.md) для більш детальної інформації про `allowable_tags`

### Значення, що повертаються

Повертає рядок завдовжки до `length` - 1 байт, прочитаних із файлу, на який вказує дескриптор `handle`, з вирізаними тегами HTML та PHP.

У разі виникнення помилки повертає **`false`**

### Приклади

**Приклад #1 Порядкове читання PHP-файлу**

```php
<?php
$str = <<<EOD
<html><body>
 <p>Добро пожаловать! Сегодня <?php echo(date('jS F')); ?>.</p>
</body></html>
Текст вне HTML-блока.
EOD;
file_put_contents('sample.php', $str);

$handle = @fopen("sample.php", "r");
if ($handle) {
    while (!feof($handle)) {
        $buffer = fgetss($handle, 4096);
        echo $buffer;
    }
    fclose($handle);
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Добро пожаловать! Сегодня .

Текст вне HTML-блока.
```

### Примітки

> **Зауваження**: Якщо виникають проблеми з розпізнаванням PHP кінців рядків під час читання або створення файлів на Macintosh-сумісному комп'ютері, увімкнення опції [auto\_detect\_line\_endings](filesystem.configuration.md#ini.auto-detect-line-endings)может помочь решить проблему.

### Дивіться також

-   [fgets()](function.fgets.md) \- Читає рядок із файлу
-   [fopen()](function.fopen.md) \- Відкриває файл або URL
-   [popen()](function.popen.md) \- Відкриває файловий покажчик процесу
-   [fsockopen()](function.fsockopen.md) \- Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [strip\_tags()](function.strip-tags.md) \- Видаляє теги HTML та PHP з рядка
-   [SplFileObject::fgetss()](splfileobject.fgetss.md) \- Отримати рядок із файлу та видалити теги HTML
-   Фильтр[string.strip\_tags](filters.string.md#filters.string.strip_tags)
