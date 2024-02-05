---
navigation:
  - function.cli-set-process-title.md: « cli\_set\_process\_title
  - function.extension-loaded.md: extension\_loaded »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: dl
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dl

(PHP 4, PHP 5, PHP 7, PHP 8)

dl — Завантажує PHP під час виконання

### Опис

```methodsynopsis
dl(string $extension_filename): bool
```

Завантажує модуль PHP, заданий аргументом `extension_filename`

Щоб перевірити, чи заданий модуль вже завантажений, використовуйте функцію [extension\_loaded()](function.extension-loaded.md). Функція працює як для вбудованих модулів, так і для динамічно завантажених (тобто завантажених як через php.ini, так і через **dl()**

**Увага**

Функція доступна лише для CLI та вбудованого SAPI, а також для CGI SAPI під час запуску з командного рядка.

### Список параметрів

`extension_filename`

Аргумент содержит*тільки* Ім'я файлу модуля, який потрібно завантажити. Це ім'я залежить від платформи. Наприклад, модуль [sockets](ref.sockets.md) (якщо скомпілюваний, як завантажуваний модуль, а не модуль за замовчуванням!) буде називатися sockets.so на Unix-платформах, і php\_sockets.dll у середовищі Windows.

Директорія, з якої модуль має бути завантажений, також залежить від платформи:

Windows - Якщо явно не задано в php.ini, модуль буде завантажуватися з C:\\php5\\по умолчанию.

Unix - Якщо явно не задано в php.ini, директорія за замовчуванням залежить від

-   PHP зібраний з налаштуванням`--enable-debug`або без неї
-   PHP зібраний за допомогою ZTS (Zend Thread Safety) чи ні
-   поточний внутрішній номер`ZEND_MODULE_API_NO`(Номер внутрішнього модуля Zend API, який, як правило, є датою основної зміни API модуля, наприклад`20010901`) .

Зважаючи на вищесказане, отримуємо такі значення за замовчуванням для директорії модуля `<install-dir>/lib/php/extensions/ <debug-or-not>-<zts-or-not>-ZEND_MODULE_API_NO`наприклад, /usr/local/php/lib/php/extensions/debug-non-zts-20010901 або /usr/local/php/lib/php/extensions/no-debug-zts-20010901.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо механізм завантаження модулів недоступний або вимкнений (значення off налаштування [enable\_dl](info.configuration.md#ini.enable-dl) у php.ini), буде видана помилка **`E_ERROR`** та виконання припиняється. Якщо **dl()**не сможет загрузить заданную библиотеку, то в дополнение к**`false`** буде видано повідомлення **`E_WARNING`**

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

> **Зауваження** :
> 
> **dl()** чутлива до регістру на Unix-платформах.

### Дивіться також

-   [Директиви завантаження модулів](ini.core.md#ini.extension)
-   [extension\_loaded()](function.extension-loaded.md) \- Визначає, чи завантажений модуль
