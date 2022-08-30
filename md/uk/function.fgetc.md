Зчитує символ із файлу

-   [« fflush](function.fflush.html)
    
-   [fgetcsv »](function.fgetcsv.html)
    
-   [PHP Manual](index.html)
    
-   [Функції файлової системи](ref.filesystem.html)
    
-   Зчитує символ із файлу
    

# fgetc

(PHP 4, PHP 5, PHP 7, PHP 8)

fgetc — Зчитує символ із файлу

### Опис

```methodsynopsis
fgetc(resource $stream): string|false
```

Зчитує символ із переданого покажчика на файл.

### Список параметрів

`stream`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.html) або [fsockopen()](function.fsockopen.html) (і все ще не закритий функцією [fclose()](function.fclose.html)

### Значення, що повертаються

Повертає рядок з одним символом, прочитаним із файлу, на який вказує `stream`. Повертає **`false`** при досягненні EOF.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад використання функції **fgetc()****

```php
<?php
$fp = fopen('somefile.txt', 'r');
if (!$fp) {
    echo 'Ошибка при открытии файла somefile.txt';
}
while (false !== ($char = fgetc($fp))) {
    echo "$char\n";
}
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [fread()](function.fread.html) - Бінарно-безпечне читання файлу
-   [fopen()](function.fopen.html) - Відкриває файл або URL
-   [popen()](function.popen.html) - Відкриває файловий покажчик процесу
-   [fsockopen()](function.fsockopen.html) - Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [fgets()](function.fgets.html) - Читає рядок із файлу