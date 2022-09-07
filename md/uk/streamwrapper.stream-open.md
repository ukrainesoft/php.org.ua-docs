---
navigation:
  - streamwrapper.stream-metadata.md: '« streamWrapper::streammetadata'
  - streamwrapper.stream-read.md: 'streamWrapper::streamread »'
  - index.md: PHP Manual
  - class.streamwrapper.md: streamWrapper
title: 'streamWrapper::streamopen'
---
# streamWrapper::streamopen

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamWrapper::streamopen — Відкриває файл або URL

### Опис

```methodsynopsis
public streamWrapper::stream_open(    string $path,    string $mode,    int $options,    ?string &$opened_path): bool
```

Цей метод викликається відразу після ініціалізації обгортки (наприклад, [fopen()](function.fopen.md) і [filegetcontents()](function.file-get-contents.md)

### Список параметрів

`path`

Встановлює URL-адресу, яка буде передана в функцію, що викликає.

> **Зауваження**
> 
> URL можна розділити на частини функцією [parseurl()](function.parse-url.md). URL має бути відокремлений символами ://. Символи : та :/ поки працюють, але подальша підтримка не гарантується.

`mode`

Режим відкриття файлу, аналогічний режимам для [fopen()](function.fopen.md)

> **Зауваження**
> 
> Не забувайте перевіряти, чи підтримується режим `mode` файлом `path`

`options`

Зберігає додаткові прапори, що задаються API потоків. Може містити одне або кілька значень, які об'єднані операцією АБО. Значення наведені нижче.

| Флаг | Описание |
| --- | --- |
| **`STREAM_USE_PATH`** | Якщо шлях `path` відносний, потрібно шукати ресурс, використовуючи includepath. |
| **`STREAM_REPORT_ERRORS`** | Якщо цей прапор задано, Ви можете викликати помилки функцією [triggererror()](function.trigger-error.md) під час відкриття потоку. Якщо прапор не встановлено, помилки викликати не можна. |

`opened_path`

Якщо `path` успішно відкритий, та **`STREAM_USE_PATH`** задана в `options`, то в аргументі `opened_path` необхідно зберегти повний шлях до відкритого файлу чи ресурсу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо виклик до цього методу не вдалося (наприклад, не реалізовано).

### Примітки

> **Зауваження**
> 
> Властивість streamWrapper::$context буде оновлено, якщо коректний контекст був переданий у функцію, що викликається.

### Дивіться також

-   [fopen()](function.fopen.md) - Відкриває файл або URL
-   [parseurl()](function.parse-url.md) - Розбирає URL та повертає його компоненти
