---
navigation:
  - function.cli-set-process-title.md: « clisetprocesstitle
  - function.extension-loaded.md: extensionloaded »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: дл
---
# дл

(PHP 4, PHP 5, PHP 7, PHP 8)

dl — Завантажує PHP під час виконання

### Опис

```methodsynopsis
dl(string $extension_filename): bool
```

Завантажує модуль PHP, заданий аргументом `extension_filename`

Щоб перевірити, чи заданий модуль вже завантажений, використовуйте функцію [extensionloaded()](function.extension-loaded.md). Функція працює як для вбудованих модулів, так і для динамічно завантажених (тобто завантажених як через php.ini, так і через **dl()**

**Увага**

Функція видалена з деяких SAPI PHP 5.3.0 і видалена з PHP-FPM в PHP 7.0.0.

### Список параметрів

`extension_filename`

Аргумент містить *тільки* Ім'я файлу модуля, який потрібно завантажити. Це ім'я залежить від платформи. Наприклад, модуль [sockets](ref.sockets.md) (якщо скомпільований, як завантажуваний модуль, а не модуль за замовчуванням!) буде називатися sockets.so на Unix-платформах, і phpsockets.dll у середовищі Windows.

Директорія, з якої модуль має бути завантажений, також залежить від платформи:

Windows - Якщо явно не задано в php.ini, модуль буде завантажуватися з C:php5 за замовчуванням.

Unix - Якщо явно не задано в php.ini, директорія за замовчуванням залежить від

-   PHP зібраний з налаштуванням `--enable-debug` чи без неї
-   PHP зібраний з (експериментальною) підтримкою ZTS (Zend Thread Safety) чи ні
-   поточний внутрішній номер `ZEND_MODULE_API_NO` (Номер внутрішнього модуля Zend API, який, як правило, є датою основної зміни API модуля, наприклад `20010901`

Зважаючи на вищесказане, отримуємо такі значення за замовчуванням для директорії модуля `<install-dir>/lib/php/extensions/ <debug-or-not>-<zts-or-not>-ZEND_MODULE_API_NO`наприклад, /usr/local/php/lib/php/extensions/debug-non-zts-20010901 або /usr/local/php/lib/php/extensions/no-debug-zts-20010901.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо механізм завантаження модулів недоступний або вимкнений (значення off налаштування [enableдл](info.configuration.md#ini.enable-dl) у php.ini), буде видана помилка **`E_ERROR`** та виконання припиняється. Якщо **dl()** не зможе завантажити задану бібліотеку, то на додаток до **`false`** буде видано повідомлення **`E_WARNING`**

### Приклади

**Приклад #1 Приклади використання **dl()****

```php
<?php
// Пример загрузки модуля, основываясь на ОС
if (!extension_loaded('sqlite')) {
    if (strtoupper(substr(PHP_OS, 0, 3)) === 'WIN') {
        dl('php_sqlite.dll');
    } else {
        dl('sqlite.so');
    }
}

// Или на константе PHP_SHLIB_SUFFIX
if (!extension_loaded('sqlite')) {
    $prefix = (PHP_SHLIB_SUFFIX === 'dll') ? 'php_' : '';
    dl($prefix . 'sqlite.' . PHP_SHLIB_SUFFIX);
}
?>
```

### Примітки

> **Зауваження**
> 
> **dl()** чутлива до регістру на Unix-платформах.

### Дивіться також

-   [Директиви завантаження модулів](ini.core.md#ini.extension)
-   [extensionloaded()](function.extension-loaded.md) - Визначає, чи завантажений модуль
