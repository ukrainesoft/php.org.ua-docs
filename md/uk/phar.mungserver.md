---
navigation:
  - phar.mount.md: '« Phar::mount'
  - phar.offsetexists.md: 'Phar::offsetExists »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::mungServer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::mungServer

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::mungServer — Визначити список до чотирьох $\_SERVER-змінних, які мають бути змінені для запуску

### Опис

```methodsynopsis
final public static Phar::mungServer(array $variables): void
```

Функция**Phar::mungServer()** повинна викликатися лише у завантажувачі.

Визначає список до чотирьох [$\_SERVER](reserved.variables.server.md)\-змінних, які потрібно модифікувати для запуску. Модифікація полягає у видаленні слідів запуску з phar-архіву для змінних `REQUEST_URI` `PHP_SELF` `SCRIPT_NAME`и`SCRIPT_FILENAME`

Сам собою цей метод нічого не робить. Ефект досягається тільки в комбінації з [Phar::webPhar()](phar.webphar.md) і лише якщо запитаний файл є PHP-файлом для аналізу. Зверніть увагу, що змінні `PATH_INFO`и`PATH_TRANSLATED` завжди модифіковані.

Оригінальні значення змінних змінних будуть збережені в масиві SERVER з префіксами `PHAR_`. Наприклад, оригінальне значення `SCRIPT_NAME` буде записано в `PHAR_SCRIPT_NAME`

### Список параметрів

`variables`

Масив будь-якого з рядків: `REQUEST_URI` `PHP_SELF` `SCRIPT_NAME`и`SCRIPT_FILENAME`. Будь-які інші значення викликають виняток. Зверніть увагу, що функція **Phar::mungServer()** чутлива до регістру символів.

### Значення, що повертаються

Нічого не вертає.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо вхідні дані неправильні.

### Приклади

**Пример #1 Пример использования**Phar::mungServer()\*\*\*\*

```php
<?php
// пример загрузчика
Phar::mungServer(array('REQUEST_URI'));
Phar::webPhar();
__HALT_COMPILER();
?>
```

### Дивіться також

-   [Phar::webPhar()](phar.webphar.md) \- Надсилає запит із браузера у внутрішній файл у phar-архіві
-   [Phar::setStub()](phar.setstub.md) \- Встановити завантажувач або завантажувальну заглушку в Phar-архів
