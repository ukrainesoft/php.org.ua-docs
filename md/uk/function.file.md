Читає вміст файлу та поміщає його в масив

-   [« file\_put\_contents](function.file-put-contents.html)
    
-   [fileatime »](function.fileatime.html)
    
-   [PHP Manual](index.html)
    
-   [Функции файловой системы](ref.filesystem.html)
    
-   Читає вміст файлу та поміщає його в масив
    

# file

(PHP 4, PHP 5, PHP 7, PHP 8)

file - Читає вміст файлу і поміщає його в масив

### Опис

```methodsynopsis
file(string $filename, int $flags = 0, ?resource $context = null): array|false
```

Читає вміст файлу та поміщає його у масив.

> **Зауваження**
> 
> Можна також використовувати функцію [file\_get\_contents()](function.file-get-contents.html) для отримання файлу у вигляді рядка.

### Список параметрів

`filename`

Шлях до файлу.

**Підказка**

Для цієї функції ви можете використовувати URL як ім'я файлу, якщо була увімкнена опція [fopen wrappers](filesystem.configuration.html#ini.allow-url-fopen). Докладніше про визначення імені файлу в описі функції [fopen()](function.fopen.html). Дивіться також список оберток URL, що підтримуються, їх можливості, зауваження щодо використання та список визначених констант у розділі [Поддерживаемые протоколы и обёртки](wrappers.html)

`flags`

Як необов'язковий параметр `flags` може вказати одну або більше наступних констант:

**`FILE_USE_INCLUDE_PATH`**

Шукає файл у [include\_path](ini.core.html#ini.include-path)

**`FILE_IGNORE_NEW_LINES`**

Пропускати новий рядок наприкінці кожного елемента масиву

**`FILE_SKIP_EMPTY_LINES`**

Пропускати порожні рядки

`context`

Ресурс (resource) з [контекстом потока](stream.contexts.html)

### Значення, що повертаються

Повертає файл як масиву. Кожен елемент масиву відповідає рядку файлу з символами нового рядка включно. У разі помилки **file()** повертає **`false`**

> **Зауваження**
> 
> Кожен рядок в отриманому масиві завершуватиметься символами кінця рядка, якщо тільки не використовується **`FILE_IGNORE_NEW_LINES`**

> **Зауваження**: Якщо у вас виникають проблеми з розпізнаванням PHP кінців рядків при читанні або створенні файлів на Macintosh-сумісному комп'ютері, увімкнення опції [auto\_detect\_line\_endings](filesystem.configuration.html#ini.auto-detect-line-endings) може допомогти вирішити проблему.

### Помилки

Викликає помилку рівня **`E_WARNING`**якщо файл не існує.

### Приклади

**Приклад #1 Приклад використання **file()****

```php
<?php
// Получает содержимое файла в виде массива. В данном примере мы используем
// обращение по протоколу HTTP для получения HTML-кода с удалённого сервера.
$lines = file('http://www.example.com/');

// Осуществим проход массива и выведем содержимое в виде HTML-кода вместе с номерами строк.
foreach ($lines as $line_num => $line) {
    echo "Строка #<b>{$line_num}</b> : " . htmlspecialchars($line) . "<br />\n";
}

// Используем необязательный параметр flags
$trimmed = file('somefile.txt', FILE_IGNORE_NEW_LINES | FILE_SKIP_EMPTY_LINES);
?>
```

### Примітки

**Увага**

При використанні SSL Microsoft IIS порушує протокол, закриваючи з'єднання без надсилання індикатора `close_notify`. PHP повідомить про це як "SSL: Fatal Protocol Error" в той момент, коли ви досягнете кінця даних. Щоб обійти це, ви повинні встановити [error\_reporting](errorfunc.configuration.html#ini.error-reporting) на рівень, що виключає EWARNING. PHP вміє визначати, що на стороні сервера перебуває проблемний IIS при відкритті потоку за допомогою обгортки `https://` та не виводить попередження. Якщо ви використовуєте [fsockopen()](function.fsockopen.html) для створення `ssl://` сокету, ви самі відповідаєте за визначення та придушення цього попередження.

### Дивіться також

-   [file\_get\_contents()](function.file-get-contents.html) - Читає вміст файлу в рядок
-   [readfile()](function.readfile.html) - Виводить файл
-   [fopen()](function.fopen.html) - Відкриває файл або URL
-   [fsockopen()](function.fsockopen.html) - Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [popen()](function.popen.html) - Відкриває файловий покажчик процесу
-   [include](function.include.html) - include
-   [stream\_context\_create()](function.stream-context-create.html) - Створює контекст потоку