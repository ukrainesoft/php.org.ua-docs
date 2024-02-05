---
navigation:
  - function.fflush.md: « fflush
  - function.fgetcsv.md: fgetcsv »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: fgetc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.md) або [fsockopen()](function.fsockopen.md) (і все ще не закритий функцією [fclose()](function.fclose.md)

### Значення, що повертаються

Повертає рядок з одним символом, прочитаним із файлу, на який вказує `stream`. Повертає \*\*`false`\*\*при достижении EOF.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Приклад использования функции**fgetc()\*\*\*\*

```php
<?php
$fp = fopen('somefile.txt', 'r');
if (!$fp) {
    echo 'Ошибка при открытии файла somefile.txt';
}
while (false !== ($char = fgetc($fp))) {
    echo "$char\n";
}
?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [fread()](function.fread.md) \- Бінарно-безпечне читання файлу
-   [fopen()](function.fopen.md) \- Відкриває файл або URL
-   [popen()](function.popen.md) \- Відкриває файловий покажчик процесу
-   [fsockopen()](function.fsockopen.md) \- Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [fgets()](function.fgets.md) \- Читає рядок із файлу
