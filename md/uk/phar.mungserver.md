Визначити список до чотирьох $SERVER-змінних, які мають бути змінені для запуску

-   [« Phar::mount](phar.mount.html)
    
-   [Phar::offsetExists »](phar.offsetexists.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Визначити список до чотирьох $SERVER-змінних, які мають бути змінені для запуску
    

# Phar::mungServer

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::mungServer — Визначити список до чотирьох $SERVER-змінних, які мають бути змінені для запуску

### Опис

```methodsynopsis
final public static Phar::mungServer(array $variables): void
```

Функція **Phar::mungServer()** повинна викликатися лише у завантажувачі.

Визначає список до чотирьох [$\_SERVER](reserved.variables.server.html)змінних, які потрібно модифікувати для запуску. Модифікація полягає у видаленні слідів запуску з phar-архіву для змінних `REQUEST_URI` `PHP_SELF` `SCRIPT_NAME` і `SCRIPT_FILENAME`

Сам собою цей метод нічого не робить. Ефект досягається тільки в комбінації з [Phar::webPhar()](phar.webphar.html) і лише якщо запитаний файл є PHP-файлом для аналізу. Зверніть увагу, що змінні `PATH_INFO` і `PATH_TRANSLATED` завжди модифіковані.

Оригінальні значення змінних змінних будуть збережені в масиві SERVER з префіксами `PHAR_`. Наприклад, оригінальне значення `SCRIPT_NAME` буде записано в `PHAR_SCRIPT_NAME`

### Список параметрів

`variables`

Масив, що містить комбінацію з: `REQUEST_URI` `PHP_SELF` `SCRIPT_NAME` і `SCRIPT_FILENAME`. Будь-які інші значення викликають виняток. Зверніть увагу, що функція **Phar::mungServer()** чутлива до регістру символів.

### Значення, що повертаються

Нічого не вертає.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.html), якщо вхідні дані неправильні.

### Приклади

**Приклад #1 Приклад використання **Phar::mungServer()****

```php
<?php
// пример загрузчика
Phar::mungServer(array('REQUEST_URI'));
Phar::webPhar();
__HALT_COMPILER();
?>
```

### Дивіться також

-   [Phar::webPhar()](phar.webphar.html) - Надсилає запит із браузера у внутрішній файл у phar-архіві
-   [Phar::setStub()](phar.setstub.html) - Встановити завантажувач або завантажувальну заглушку в Phar-архів