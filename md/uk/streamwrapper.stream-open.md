---
navigation:
  - streamwrapper.stream-metadata.md: '« streamWrapper::stream\_metadata'
  - streamwrapper.stream-read.md: 'streamWrapper::stream\_read »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::stream\_open'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# streamWrapper::stream\_open

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::stream\_open — Відкриває файл або URL

### Опис

```methodsynopsis
public streamWrapper::stream_open(    string $path,    string $mode,    int $options,    ?string &$opened_path): bool
```

Цей метод викликається відразу після ініціалізації обгортки (наприклад, [fopen()](function.fopen.md) і [file\_get\_contents()](function.file-get-contents.md)

### Список параметрів

`path`

Встановлює URL-адресу, яка буде передана в функцію, що викликає.

> **Зауваження** :
> 
> URL можна розділити на частини функцією [parse\_url()](function.parse-url.md). URL має бути відокремлений символами ://. Символи : та :/ поки працюють, але подальша підтримка не гарантується.

`mode`

Режим відкриття файлу, аналогічний режимам для [fopen()](function.fopen.md)

> **Зауваження** :
> 
> Не забувайте перевіряти, чи підтримується режим `mode`файлом`path`

`options`

Зберігає додаткові прапори, що задаються API потоків. Може містити одне або кілька значень, які об'єднані операцією АБО. Значення наведені нижче.

| Флаг | Опис |
| --- | --- |
| **`STREAM_USE_PATH`** | Якщо шлях `path` відносний, потрібно шукати ресурс, використовуючи include\_path. |
| **`STREAM_REPORT_ERRORS`** | Якщо цей прапор задано, Ви можете викликати помилки функцією [trigger\_error()](function.trigger-error.md) під час відкриття потоку. Якщо прапор не встановлено, помилки викликати не можна. |

`opened_path`

Якщо `path` успішно відкритий, та \*\*`STREAM_USE_PATH`\*\*задана в`options`, то в аргументе`opened_path` необхідно зберегти повний шлях до відкритого файлу чи ресурсу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Примітки

> **Зауваження** :
> 
> Властивість streamWrapper::$context буде оновлено, якщо коректний контекст був переданий у функцію, що викликається.

### Дивіться також

-   [fopen()](function.fopen.md) \- Відкриває файл або URL
-   [parse\_url()](function.parse-url.md) \- Розбирає URL та повертає його компоненти
