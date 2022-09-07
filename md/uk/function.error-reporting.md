---
navigation:
  - function.error-log.md: « errorlog
  - function.restore-error-handler.md: restoreerrorhandler »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функции обработки ошибок
title: errorreporting
---
# errorreporting

(PHP 4, PHP 5, PHP 7, PHP 8)

errorreporting — Задає, які помилки PHP потраплять у звіт

### Опис

```methodsynopsis
error_reporting(?int $error_level = null): int
```

Функція **errorreporting()** задає значення директиви [errorreporting](errorfunc.configuration.md#ini.error-reporting) під час виконання. У PHP є багато рівнів помилок. Використовуючи цю функцію, можна встановити рівень помилок часу виконання скрипта, які попадуть у звіт. Якщо необов'язковий аргумент `error_level` не заданий, **errorreporting()** поверне поточне значення рівня протоколювання помилок.

### Список параметрів

`error_level`

Нове значення рівня [errorreporting](errorfunc.configuration.md#ini.error-reporting). Це може бути бітова маска чи іменовані константи. При використанні іменованих констант потрібно буде стежити за сумісністю з новими версіями PHP. У нових версіях можуть додатись нові рівні помилок, збільшитися діапазон цілих типів. Все це може призвести до нестабільної роботи з використанням старих цілочисельних позначень рівнів помилок.

Доступні константи рівнів помилок та їх опис наведено в розділі [Обумовлені константи](errorfunc.constants.md)

### Значення, що повертаються

Повертає старе значення рівня [errorreporting](errorfunc.configuration.md#ini.error-reporting) або поточне значення, якщо аргумент `error_level` не заданий.

### список змін

| Версия | Описание |
| --- | --- |
|  | `error_level` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклади використання **errorreporting()****

```php
<?php

// Выключение протоколирования ошибок
error_reporting(0);

// Включать в отчёт простые описания ошибок
error_reporting(E_ERROR | E_WARNING | E_PARSE);

// Включать в отчёт E_NOTICE сообщения (добавятся сообщения о
// непроинициализированных переменных или ошибках в именах переменных)
error_reporting(E_ERROR | E_WARNING | E_PARSE | E_NOTICE);

// Добавлять сообщения обо всех ошибках, кроме E_NOTICE
error_reporting(E_ALL & ~E_NOTICE);

// Добавлять в отчёт все ошибки PHP
error_reporting(E_ALL);

// Добавлять в отчёт все ошибки PHP
error_reporting(-1);

// То же, что и error_reporting(E_ALL);
ini_set('error_reporting', E_ALL);

?>
```

### Примітки

**Підказка**

Якщо передати `-1`, будуть відображатися всі можливі помилки, навіть якщо до нових версій PHP додадуться рівні або константи. Поведінка еквівалентна передачі константи **`E_ALL`**

### Дивіться також

-   Директива [displayerrors](errorfunc.configuration.md#ini.display-errors)
-   Директива [htmlerrors](errorfunc.configuration.md#ini.html-errors)
-   Директива [xmlrpcerrors](errorfunc.configuration.md#ini.xmlrpc-errors)
-   [iniset()](function.ini-set.md) - Встановлює налаштування конфігурації
