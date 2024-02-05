---
navigation:
  - function.error-log.md: « error\_log
  - function.restore-error-handler.md: restore\_error\_handler »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функції обробки помилок
title: error\_reporting
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# error\_reporting

(PHP 4, PHP 5, PHP 7, PHP 8)

error\_reporting - Встановлює, які помилки PHP потраплять у звіт

### Опис

```methodsynopsis
error_reporting(?int $error_level = null): int
```

Функция**error\_reporting()** задає значення директиви [error\_reporting](errorfunc.configuration.md#ini.error-reporting) під час роботи (виконання) програми. PHP містить багато рівнів помилок. Через цю функцію задають рівень помилок на час роботи (виконання) скрипта, які потраплять у звіт. Якщо необов'язковий аргумент `error_level`не задан, функция**error\_reporting()** поверне поточне значення рівня протоколювання помилок.

### Список параметрів

`error_level`

Новое значение уровня[error\_reporting](errorfunc.configuration.md#ini.error-reporting). Параметр приймає або бітову маску, або іменовані константи. При вказанні іменованих констант потрібно буде стежити за сумісністю з новими версіями PHP. У міру додавання рівнів помилок діапазон цілих чисел збільшується, тому старі рівні помилок на основі цілих чисел не завжди поводитимуться передбачувано.

Доступні константи рівнів помилок та їх описи наведено у розділі « [Обумовлені константи](errorfunc.constants.md) ».

### Значення, що повертаються

Повертає значення директиви [error\_reporting](errorfunc.configuration.md#ini.error-reporting), яке в ній зберігалося *до того*, як було змінено значення параметра `error_level`

> **Зауваження**: Оператор[управління помилками](language.operators.errorcontrol.md) `@`) изменяет значение параметра`error_level`во время обработки ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`error_level` тепер може набувати значення null. |

### Приклади

**Приклад #1 Приклад використання функції **error\_reporting()****

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

Якщо передати значення `-1`, будуть відображатися всі можливі помилки, навіть якщо до нових версій PHP додадуться рівні або константи. Поведінка еквівалентна передачі константи **`E_ALL`**

### Дивіться також

-   Директива[display\_errors](errorfunc.configuration.md#ini.display-errors)
-   Директива[html\_errors](errorfunc.configuration.md#ini.md-errors)
-   Директива[xmlrpc\_errors](errorfunc.configuration.md#ini.xmlrpc-errors)
-   Оператор[управління помилками](language.operators.errorcontrol.md)
-   Функция[ini\_set()](function.ini-set.md) \- Встановлює налаштування конфігурації — Встановлює значення налаштування конфігурації
