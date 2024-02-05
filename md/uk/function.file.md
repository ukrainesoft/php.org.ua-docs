---
navigation:
  - function.file-put-contents.md: « file\_put\_contents
  - function.fileatime.md: fileatime »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# file

(PHP 4, PHP 5, PHP 7, PHP 8)

file - Читає вміст файлу і поміщає його в масив

### Опис

```methodsynopsis
file(string $filename, int $flags = 0, ?resource $context = null): array|false
```

Читає вміст файлу та поміщає його у масив.

> **Зауваження** :
> 
> Можна також використовувати функцію [file\_get\_contents()](function.file-get-contents.md) для отримання файлу у вигляді рядка.

### Список параметрів

`filename`

Шлях до файлу.

**Підказка**

У цю функцію як ім'я файлу можна передавати URL-адреси, якщо була включена директива [fopen wrappers](filesystem.configuration.md#ini.allow-url-fopen). Докладніше про те, як вказати ім'я файлу, описано в описі функції [fopen()](function.fopen.md). В розділі "[Підтримувані протоколи та обгортки](wrappers.md)» також дано посилання на інформацію про можливості підтримуваних обгорток, зауваження щодо роботи з ними та список визначених змінних, які вони дають.

`flags`

Як необов'язковий параметр `flags` може вказати одну або більше наступних констант:

**`FILE_USE_INCLUDE_PATH`**

Шукає файл у [include\_path](ini.core.md#ini.include-path)

**`FILE_IGNORE_NEW_LINES`**

Пропускати новий рядок наприкінці кожного елемента масиву

**`FILE_SKIP_EMPTY_LINES`**

Пропускати порожні рядки

**`FILE_NO_DEFAULT_CONTEXT`**

Не використовувати контекст за замовчуванням

`context`

Ресурс (resource) с[контекстом потоку](stream.contexts.md)

### Значення, що повертаються

Повертає файл як масиву. Кожен елемент масиву відповідає рядку файлу з символами нового рядка включно. У разі помилки **file()** повертає **`false`**

> **Зауваження** :
> 
> Кожен рядок в отриманому масиві завершуватиметься символами кінця рядка, якщо тільки не використовується **`FILE_IGNORE_NEW_LINES`**

> **Зауваження**: Якщо виникають проблеми з розпізнаванням PHP кінців рядків під час читання або створення файлів на Macintosh-сумісному комп'ютері, увімкнення опції [auto\_detect\_line\_endings](filesystem.configuration.md#ini.auto-detect-line-endings)может помочь решить проблему.

### Помилки

Викликає помилку рівня \*\*`E_WARNING`\*\*якщо файл не існує.

### Приклади

**Пример #1 Пример использования**file()\*\*\*\*

```php
<?php
// Получает содержимое файла в виде массива. В данном примере мы используем
// обращение по протоколу HTTP для получения HTML-кода с удалённого сервера.
$lines = file('http://www.example.com/');

// Осуществим проход массива и выведем содержимое в виде HTML-кода вместе с номерами строк.
foreach ($lines as $line_num => $line) {
    echo "Строка #<b>{$line_num}</b> : " . htmlspecialchars($line) . "<br />\n";
}

// Используем необязательный параметр flags
$trimmed = file('somefile.txt', FILE_IGNORE_NEW_LINES | FILE_SKIP_EMPTY_LINES);
?>
```

### Примітки

**Увага**

При використанні SSL Microsoft IIS порушує протокол, закриваючи з'єднання без надсилання індикатора `close_notify`. PHP повідомить про це як "SSL: Fatal Protocol Error" в той момент, коли буде досягнуто кінця даних. Щоб обійти це, потрібно встановити директиву [error\_reporting](errorfunc.configuration.md#ini.error-reporting)на уровень, исключающий E\_WARNING. PHP вміє визначати, що на стороні сервера проблемний IIS при відкритті потоку обгорткою `https://` та не виводить попередження. Якщо розробник створює сокет `ssl://` через виклик функції [fsockopen()](function.fsockopen.md), він сам відповідає за визначення та придушення цього попередження.

### Дивіться також

-   [file\_get\_contents()](function.file-get-contents.md) \- Читає вміст файлу в рядок
-   [readfile()](function.readfile.md) \- Виводить файл
-   [fopen()](function.fopen.md) \- Відкриває файл або URL
-   [fsockopen()](function.fsockopen.md) \- Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [popen()](function.popen.md) \- Відкриває файловий покажчик процесу
-   [include](function.include.md) \- include
-   [stream\_context\_create()](function.stream-context-create.md) \- Створює контекст потоку
