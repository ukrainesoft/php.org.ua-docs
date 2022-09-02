---
navigation:
  - function.fgetcsv.md: « fgetcsv
  - function.fgetss.md: fgetss »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: fgets
---
# fgets

(PHP 4, PHP 5, PHP 7, PHP 8)

fgets — Читає рядок із файлу

### Опис

```methodsynopsis
fgets(resource $stream, ?int $length = null): string|false
```

Читає рядок із файлового покажчика.

### Список параметрів

`stream`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.md) або [fsockopen()](function.fsockopen.md) (і все ще не закритий функцією [fclose()](function.fclose.md)

`length`

Читання закінчується при досягненні `length` - 1 байт, або якщо зустрівся новий рядок (який включається в результат, що повертається) або кінець файлу (залежно від того, що настане раніше). Якщо довжина не вказана, читання з потоку триватиме доти, доки досягне кінця рядка.

### Значення, що повертаються

Повертає рядок розміром у `length` - 1 байт, прочитаний з дескриптора файлу, на який вказує параметр `stream`. Якщо даних для читання більше немає, то повертає **`false`**

У разі виникнення помилки повертає **`false`**

### Приклади

**Приклад #1 Порядкове читання файлу**

```php
<?php
$fp = @fopen("/tmp/inputfile.txt", "r");
if ($fp) {
    while (($buffer = fgets($fp, 4096)) !== false) {
        echo $buffer;
    }
    if (!feof($fp)) {
        echo "Ошибка: fgets() неожиданно потерпел неудачу\n";
    }
    fclose($fp);
}
?>
```

### Примітки

> **Зауваження**: Якщо у вас виникають проблеми з розпізнаванням PHP кінців рядків під час читання або створення файлів на Macintosh-сумісному комп'ютері, увімкнення опції [autodetectlineendings](filesystem.configuration.md#ini.auto-detect-line-endings) може допомогти вирішити проблему.

> **Зауваження**
> 
> Програмісти, що звикли до семантики 'C' функції **fgets()**, повинні брати до уваги різницю в тому, як повертається ознака досягнення кінця файлу (`EOF`

### Дивіться також

-   [fgetss()](function.fgetss.md) - Читає рядок з файлу та видаляє HTML-теги
-   [fread()](function.fread.md) - Бінарно-безпечне читання файлу
-   [fgetc()](function.fgetc.md) - Зчитує символ із файлу
-   [streamgetline()](function.stream-get-line.md) - Отримує рядок із потокового ресурсу до вказаного роздільника
-   [fopen()](function.fopen.md) - Відкриває файл або URL
-   [popen()](function.popen.md) - Відкриває файловий покажчик процесу
-   [fsockopen()](function.fsockopen.md) - Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [streamsettimeout()](function.stream-set-timeout.md) - Встановити значення часу очікування потоку
