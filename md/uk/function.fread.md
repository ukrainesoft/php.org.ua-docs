Бінарно-безпечне читання файлу

-   [« fputs](function.fputs.html)
    
-   [fscanf »](function.fscanf.html)
    
-   [PHP Manual](index.html)
    
-   [Функции файловой системы](ref.filesystem.html)
    
-   Бінарно-безпечне читання файлу
    

# fread

(PHP 4, PHP 5, PHP 7, PHP 8)

fread — Бінарно-безпечне читання файлу

### Опис

```methodsynopsis
fread(resource $stream, int $length): string|false
```

**fread()** читає до `length` байт із файлового покажчика `stream` та зміщує покажчик. Читання зупиняється як тільки було досягнуто однієї з наступних умов:

-   було прочитано `length` байт
-   досягнуто EOF (кінець файлу)
-   став доступний пакет або минув [время ожидания сокета](function.socket-set-timeout.html) (для мережевих потоків)
-   якщо потік, що читається, є буферизованим і не являє собою звичайний файл, то за один раз максимум читається кількість байт, рівну розміру однієї порції даних (зазвичай це 8192), однак, залежно від раніше буферизованих даних розмір даних, що повертаються, може бути більше розміру однієї порції даних .

### Список параметрів

`stream`

Вказівник (resource) на файл, який зазвичай створюється за допомогою функції [fopen()](function.fopen.html)

`length`

`length` вказує розмір прочитаних даних у байтах.

### Значення, що повертаються

Повертає прочитаний рядок або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Простий приклад використання **fread()****

```php
<?php
// получает содержимое файла в строку
$filename = "/usr/local/something.txt";
$handle = fopen($filename, "r");
$contents = fread($handle, filesize($filename));
fclose($handle);
?>
```

**Приклад #2 Приклад бінарного читання за допомогою **fread()****

**Увага**

На системах, які розрізняють бінарні та текстові файли (наприклад, Windows), файл повинен бути відкритий за допомогою прапора 'b' у параметрі mode функції [fopen()](function.fopen.html)

```php
<?php
$filename = "c:\\files\\somepic.gif";
$handle = fopen($filename, "rb");
$contents = fread($handle, filesize($filename));
fclose($handle);
?>
```

**Приклад #3 Приклади віддаленого читання за допомогою **fread()****

**Увага**

При читанні чогось відмінного від локальних файлів, наприклад потоків, що повертаються під час читання [удалённых файлов](features.remote-files.html) або з [popen()](function.popen.html) і [fsockopen()](function.fsockopen.html), читання зупиниться після того, як пакет стане доступним. Це означає, що ви повинні збирати дані разом на шматочки, як показано на прикладі нижче.

```php
<?php
$handle = fopen("http://www.example.com/", "rb");
$contents = stream_get_contents($handle);
fclose($handle);
?>
```

```php
<?php
$handle = fopen("http://www.example.com/", "rb");
if (FALSE === $handle) {
    exit("Не удалось открыть поток по url адресу");
}

$contents = '';

while (!feof($handle)) {
    $contents .= fread($handle, 8192);
}
fclose($handle);
?>
```

### Примітки

> **Зауваження**
> 
> Якщо ви просто хочете отримати вміст файлу у вигляді рядка, використовуйте [file\_get\_contents()](function.file-get-contents.html), оскільки ця функція набагато продуктивніша, ніж описаний вище код.

> **Зауваження**
> 
> Врахуйте, що **fread()** читає, починаючи з поточної позиції файлового покажчика. Використовуйте функцію [ftell()](function.ftell.html) для знаходження поточної позиції покажчика та функцію [rewind()](function.rewind.html) для перемотування позиції покажчика на початок.

### Дивіться також

-   [fwrite()](function.fwrite.html) - Бінарно-безпечний запис у файл
-   [fopen()](function.fopen.html) - Відкриває файл або URL
-   [fsockopen()](function.fsockopen.html) - Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [popen()](function.popen.html) - Відкриває файловий покажчик процесу
-   [fgets()](function.fgets.html) - Читає рядок із файлу
-   [fgetss()](function.fgetss.html) - Читає рядок з файлу та видаляє HTML-теги
-   [fscanf()](function.fscanf.html) - Обробляє дані з файлу відповідно до формату
-   [file()](function.file.html) - Читає вміст файлу та поміщає його в масив
-   [fpassthru()](function.fpassthru.html) - Виводить всі дані з файлового покажчика, що залишилися.
-   [fseek()](function.fseek.html) - Встановлює зміщення у файловому покажчику
-   [ftell()](function.ftell.html) - Повертає поточну позицію покажчика читання/запису файлу
-   [rewind()](function.rewind.html) - Скидає курсор файлового покажчика
-   [unpack()](function.unpack.html) - Розпакувати дані з бінарного рядка